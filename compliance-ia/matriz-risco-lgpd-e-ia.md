---
document_id: "LGPD-RIPD-001"
title: "Matriz de Risco LGPD, Marco Legal da IA e Limites de Responsabilidade Civil"
version: "1.0.0"
author: "André (Diretoria Jurídica & LegalOps)"
co_reviewers:
  - "Adriana (Diretoria de Farmácia & Regulatório Anvisa)"
  - "Antônio (Engenharia de IA)"
  - "Anderson (Arquitetura de Dados & Segurança)"
legal_framework:
  - "Lei nº 13.709/2018 (LGPD - especialmente Arts. 6º, 11, 20 e 38)"
  - "PL nº 2.338/2023 (Marco Legal da Inteligência Artificial no Brasil)"
  - "RDC Anvisa nº 657/2022 (Software como Dispositivo Médico - SaMD / Apoio Clínico)"
---

# 🛡️ Matriz de Risco LGPD & Governança de Inteligência Artificial (RIPD)

## 1. Escopo e Finalidade do Relatório (Art. 38 da LGPD)
Este Relatório de Impacto à Proteção de Dados Pessoais (RIPD) e Matriz de Risco de IA estabelece as salvaguardas jurídicas e técnicas para os agentes autônomos desenvolvidos no repositório [`fratuci-labs/ai-agents-core`](https://github.com/fratuci-labs/ai-agents-core) e auditados em [`fratuci-labs/gcp-data-foundation`](https://github.com/fratuci-labs/gcp-data-foundation).

---

## 2. Classificação de Risco dos Sistemas de IA da Fratuci Labs

| Sistema / Agente | Vertical | Classificação de Risco | Dados Pessoais Sensíveis? | Medida Jurídica & Técnica Obrigatória |
| :--- | :--- | :---: | :---: | :--- |
| **Agente de Triagem Farmacológica (`PHARMA-TRIAGE-001`)** | HealthTech | **ALTO RISCO** | **Não** (Opera sobre princípios ativos DCB/DCI anonimizados) | Proibição estrita de prescrição médica; RAG restrito à base curada da Adriana; supervisão humana obrigatória (*Human-in-the-Loop*) em alertas de severidade `ALTA`. |
| **Ponte Gemini-to-GitHub (`gemini-webhook-ingest`)** | Plataforma Interna | **BAIXO RISCO** | **Não** (Apenas documentos corporativos dos sócios) | Assinatura HMAC-SHA256 obrigatória (fail-closed), restrição de organização `fratuci-labs` e revisão via Pull Request. |
| **Motor de Anomalias Logísticas (`LOGTECH-PREDICT`)** | LogTech | **RISCO MODERADO** | **Minimizado** (Telemetria de carga e cadeia fria) | Pseudonimização de identificadores de motoristas; retenção controlada por TTL no ClickHouse. |

---

## 3. Conformidade com o Art. 20 da LGPD (Revisão de Decisões Automatizadas)

> [!IMPORTANT]
> **Art. 20 da LGPD:** *"O titular dos dados tem direito a solicitar a revisão de decisões tomadas unicamente com base em tratamento automatizado de dados pessoais que afetem seus interesses..."*

Para garantir conformidade plena e blindar a responsabilidade civil da **Fratuci Labs**:
1. **Inexistência de Decisão Clínica Autônoma:** Nossos sistemas na vertical de Saúde/Farmácia atuam exclusivamente como **Ferramenta de Suporte à Decisão Clínica e Farmacêutica (Informativa)**. A decisão final cabe 100% ao profissional habilitado (Farmacêutico CRF ou Médico CRM).
2. **Explicabilidade Determinística:** Diferente de LLMs puros ("caixa-preta"), o agente do **Antônio** é obrigado a citar o código DCB, o mecanismo de interação e a fonte regulatória exata cadastrada pela **Adriana** em `interacoes-medicamentosas-criticas.json`.
3. **Trilha de Auditoria Criptográfica (5 Anos):** A tabela `fratuci_audit.healthtech_agent_events` no ClickHouse do **Anderson** preserva por 5 anos (prazo prescricional do CDC/Código Civil) o hash SHA-256 do System Prompt (`prompt_sha256`) e da base de dados (`pharma_dataset_sha256`) vigentes no exato milissegundo da resposta.

---

## 4. Texto Padrão de Aviso Legal Obrigatório (*Disclaimer* Homologado)

Todo System Prompt da vertical HealthTech deve injetar obrigatoriamente a reprodução literal do seguinte rodapé jurídico nas respostas:

> *"⚖️ **AVISO LEGAL (FRATUCI LABS — CONFORMIDADE LGPD & ANVISA):** Esta análise tem caráter estritamente informativo e de suporte técnico-farmacológico, baseada na Denominação Comum Brasileira (DCB) e na base auditada `interacoes-medicamentosas-criticas.json`. Este sistema **NÃO realiza prescrição médica ou diagnóstico clínico**, não substituindo o julgamento profissional do Médico ou Farmacêutico responsável. Em interações de severidade ALTA ou CONTRAINDICADA, a revisão e confirmação humana por profissional habilitado é obrigatória (Art. 20 da LGPD)."*
