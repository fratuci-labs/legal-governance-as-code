---
document_id: "SOC-PROTO-001"
title: "Protocolo Familiar e Acordo de Sócios da Fratuci Labs Ltda."
version: "1.1.0"
effective_date: "2026-10-25"
author: "André (Diretoria Jurídica & Governança)"
signatories:
  - "Anderson (@fratuci) — Arquitetura de Dados & Cloud"
  - "Antônio — Engenharia de IA & Agentes Autônomos"
  - "André — Diretoria Jurídica, Governança & LegalOps"
  - "Adriana — Estratégia de Negócios, Produto & Farmácia"
status: "EM REVISÃO SOCIETÁRIA (PR)"
---

# 📜 Protocolo Familiar e Acordo de Sócios — Fratuci Labs

> [!IMPORTANT]
> Este instrumento regula as relações societárias, financeiras, operacionais, de propriedade intelectual e familiares entre os 4 sócios-diretores da **Fratuci Labs**, prevenindo conflitos por meio de regras claras, objetivas e versionadas em Git.

---

## CLÁUSULA 1ª — Do Objeto, Tipo Societário e Proteção Patrimonial
1.1. A **Fratuci Labs** opera sob a forma de **Sociedade Empresária Limitada (LTDA)**, nos termos do art. 1.052 do Código Civil Brasileiro, garantindo a **separação patrimonial estrita** entre os bens pessoais dos membros da família e as obrigações da sociedade.
1.2. É expressamente vedada a confusão patrimonial: nenhuma despesa doméstica ou pessoal poderá transitar pelas contas da sociedade, assim como o orçamento de infraestrutura em nuvem (cota FinOps de US$ 100/mês gerida por **Anderson**) destina-se exclusivamente às operações técnicas da empresa.

---

## CLÁUSULA 2ª — Da Governança dos 4 Pilares e Alçadas de Decisão
Cada sócio detém autonomia técnica dentro de sua diretoria, respeitando o dever de revisão cruzada via *Pull Request*:
1. **Diretoria de Dados & Cloud (Anderson):** Soberania sobre arquitetura GCP, ClickHouse, BigQuery, segurança IAM/OIDC e travas de FinOps.
2. **Diretoria de Engenharia de IA (Antônio):** Soberania sobre motores de agentes, pipelines RAG, middlewares em Go/Rust e arquitetura de System Prompts.
3. **Diretoria Jurídica & LegalOps (André):** Soberania sobre conformidade LGPD, contratos B2B, licenciamento de software, responsabilidade civil e governança societária.
4. **Diretoria de Estratégia, Produto & Farmácia (Adriana):** Soberania sobre seleção de verticais de mercado, roadmaps B2B, conformidade regulatória sanitária (Anvisa) e curadoria científica de bases farmacológicas.

---

## CLÁUSULA 3ª — Da Distinção Rigorosa entre Pró-Labore e Distribuição de Lucros

> [!WARNING]
> **Regra de Ouro Financeira Familiar:** Trabalho operacional se remunera com **Pró-Labore**; risco de capital e participação societária se remuneram com **Dividendos (Lucros)**. Os dois institutos jamais se confundem.

3.1. **Do Pró-Labore (Remuneração pelo Trabalho Efetivo):**
- Fará jus ao Pró-Labore o sócio que dedicar horas efetivas de execução técnica, comercial, clínica ou jurídica em projetos faturados ou em operação ativa.
- O valor do Pró-Labore será proporcional à dedicação operacional mensal comprovada em entregas no GitHub (commits, PRs, ADRs, pareceres e atendimento a clientes), incidindo os encargos legais cabíveis (INSS/IRPF).

3.2. **Da Distribuição de Lucros (Remuneração do Capital Social):**
- Após a apuração contábil trimestral, deduzidos os custos operacionais (incluindo nuvem GCP, APIs de IA, tributos e reserva legal de reinvestimento de 20%), o **Lucro Líquido** será distribuído aos sócios na proporção de suas quotas sociais, com isenção tributária nos termos da legislação vigente.

---

## CLÁUSULA 4ª — Dos Rituais Assíncronos e Resolução de Impasses
4.1. A empresa adota o modelo **100% Remoto e Assíncrono-Primeiro (*Async-First*)**:
- Toda proposta estratégica, mudança de arquitetura ou alteração contratual nasce como uma **Issue** ou **Pull Request** na organização `fratuci-labs`.
- Comentários em Pull Requests têm valor de deliberação diretiva formal.
4.2. Em matérias que envolvam risco sanitário (Anvisa) ou risco jurídico/regulatório (LGPD/Responsabilidade Civil), **Adriana** e **André** possuem **Direito de Veto Técnico (*Golden Veto*)**, impedindo o *merge* em produção até a mitigação do risco.

---

## CLÁUSULA 5ª — Das Regras de Entrada, Saída (*Vesting* & *Lock-up*) e Sucessão
5.1. A cessão de quotas a terceiros estranhos à família é **bloqueada**, vigorando o Direito de Preferência absoluto dos demais sócios familiares.
5.2. Em caso de retirada voluntária de qualquer sócio, a apuração de haveres será feita pelo valor patrimonial contábil ajustado, pago em até 24 (vinte e quatro) parcelas mensais, de modo a jamais descapitalizar o caixa operacional da **Fratuci Labs**.

---

## CLÁUSULA 6ª — Da Titularidade da Propriedade Intelectual (Códigos, Prompts, Bases Clínicas e Minutas)

> [!IMPORTANT]
> **Blindagem de Ativos Intangíveis da Fratuci Labs (Lei de Software nº 9.609/1998 e Lei de Direitos Autorais nº 9.610/1998)**

6.1. **Cessão Integral e Originária à Pessoa Jurídica:** Todos os ativos intangíveis criados, curados ou comitados pelos 4 sócios nos repositórios da organização `fratuci-labs` pertencem **exclusiva e integralmente à pessoa jurídica Fratuci Labs Ltda.**, compondo seu patrimônio imaterial e segredo de negócio (*Trade Secret*), incluindo expressamente:
1. **Ativos de Engenharia de Dados & Cloud (Anderson):** Módulos Terraform (`infra/main.tf`), schemas analíticos otimizados para ClickHouse 26.x (`clickhouse_healthtech_events.sql`), pipelines em Go/Rust e automações de FinOps;
2. **Ativos de Inteligência Artificial & Agentes (Antônio):** Arquiteturas de agentes autônomos, conectores RAG, o middleware `gemini_webhook_ingest.go` e a engenharia estrutural de **System Prompts como Código** (`pharma-triage-system-prompt.md`);
3. **Ativos Científicos, Clínicos e Estratégicos (Adriana):** Dicionários farmacológicos estruturados em DCB/DCI (`interacoes-medicamentosas-criticas.json`), Procedimentos Operacionais Padrão (`POP-001`), matrizes de severidade clínica e ADRs de modelo de negócios;
4. **Ativos Jurídicos e de Governança (André):** Matrizes de conformidade LGPD/IA (`LGPD-RIPD-001`), políticas de licenciamento open-source, templates contratuais modulares e pareceres automatizados.

6.2. **Prova de Autoria e Anterioridade via Git:** O histórico de commits assinado com hash criptográfico SHA-256 nos repositórios da `fratuci-labs` servirá como prova plena de anterioridade, cadeia de custódia e titularidade perante o INPI (Instituto Nacional da Propriedade Industrial) e terceiros contratantes.

6.3. **Preservação do Conhecimento em Caso de Saída:** Na hipótese de desligamento ou retirada de qualquer sócio (Cláusula 5ª), a sociedade manterá licença perpétua, irrevogável e exclusiva sobre todos os códigos, prompts, bases JSON e documentos já integrados à branch `main` da `fratuci-labs`, garantindo a continuidade ininterrupta dos contratos B2B vigentes.
