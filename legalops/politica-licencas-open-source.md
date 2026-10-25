---
document_id: "LEGALOPS-OSS-001"
title: "Política Corporativa de Governança de Licenças Open-Source"
version: "1.0.0"
author: "André (Diretoria Jurídica & LegalOps)"
enforced_on:
  - "fratuci-labs/gcp-data-foundation"
  - "fratuci-labs/ai-agents-core"
---

# 📜 Política de Licenças Open-Source — Proteção de Propriedade Intelectual

## 1. Objetivo Jurídico
Proteger o segredo de negócio e a propriedade intelectual dos softwares proprietários, agentes de IA e pipelines em **Go**, **Rust**, **Python** e **SQL** desenvolvidos pela **Fratuci Labs**, evitando o efeito *copyleft* contaminante ("efeito viral") que obrigaria a empresa a abrir o código-fonte de seus produtos comerciais B2B.

---

## 2. Matriz de Licenças de Dependências (Go Modules, Cargo Crates, NPM, PyPI)

### ✅ GRUPO A — Licenças Permitidas (*Allowlist* Automática)
Podem ser utilizadas livremente pelo **Anderson** e pelo **Antônio** em qualquer repositório da `fratuci-labs`, desde que mantidos os avisos de copyright originais:
- **`MIT License`**
- **`Apache License 2.0`** *(Preferencial, pois inclui cláusula expressa de concessão de patentes)*
- **`BSD 2-Clause` / `BSD 3-Clause`**
- **`ISC License`**

---

### ⚠️ GRUPO B — Licenças Restritas (Exigem Parecer Prévio do André via PR)
Permitidas apenas para bibliotecas vinculadas dinamicamente sem modificação do código-fonte da biblioteca:
- **`MPL-2.0` (Mozilla Public License 2.0)**
- **`LGPL-2.1` / `LGPL-3.0`** *(Atenção: em Go e Rust, o binário estático exige cuidado redobrado com LGPL!)*

---

### 🚫 GRUPO C — Licenças Terminantemente Bloqueadas (*Denylist* — Veto Imediato)

> [!CAUTION]
> **PROIBIÇÃO ABSOLUTA EM DEPENDÊNCIAS DE CÓDIGO:**  
> Nenhuma biblioteca em Go (`go.mod`) ou Rust (`Cargo.toml`) da Fratuci Labs pode importar pacotes sob as licenças abaixo.

- ❌ **`AGPL-3.0` (GNU Affero General Public License v3.0):**
  - **Risco Crítico para SaaS/Cloud:** A cláusula 13 da AGPL-3.0 determina que a simples disponibilização do software via rede (ex: uma API no Cloud Run) obriga a distribuição do código-fonte completo de toda a aplicação para os usuários.
- ❌ **`GPL-2.0` / `GPL-3.0` (GNU General Public License):**
  - Contaminam binários compilados estaticamente em Go e Rust.
- ❌ **`SSPL` (Server Side Public License) / `BSL` (Business Source License):**
  - Licenças restritivas que vedam oferta comercial como serviço gerenciado.

> [!NOTE]
> **Exceção de Infraestrutura Isolada:** O uso do banco de dados **ClickHouse** pelo **Anderson** é 100% seguro e aprovado, pois o ClickHouse é distribuído sob a licença permissiva **`Apache License 2.0`**.
