# Cronograma Detalhado — Processos de Software

## Bacharelado em Engenharia de Software — UFRN/DIMAp

**Período**: 2026.1 (17/03/2026 a 11/07/2026)  
**Horário**: Terças e Quintas, 10:30 às 12:00 (M56)

---

## Legenda

| Símbolo | Significado |
|---------|-------------|
| 📺 | Vídeo disponível (assistir antes da aula) |
| 🟢 | Aula presencial (atividades práticas / discussão) |
| 🔵 | Acompanhamento online (Google Meet) |
| 🚀 | Entrega de sprint/projeto |
| 📚 | Prova |
| 🔴 | Feriado/Sem aula |
| 📖 | Leitura obrigatória (ler antes do quiz) |
| 🧩 | Quiz no Multiprova (laboratório, início da aula de terça) |

---

## Calendário Resumido

| Unidade | Semanas | Período | Conteúdo Principal |
|---------|---------|---------|-------------------|
| **U1** | 1-4 | 17/03 - 10/04 | Fundamentos + Scrum + XP + Lean + Kanban |
| **U2** | 5-9 | 07/04 - 08/05 | DevOps + CI/CD + DORA + VSM + Qualidade |
| **Prova** | 10 | 12/05 | **Prova Escrita** |
| **U3** | 11-16 | 19/05 - 26/06 | Topologias de Equipe + Plataformas + IA + Padrões + Apresentações |

---

## UNIDADE 1: Fundamentos e Frameworks Ágeis (Semanas 1-4)

### Semana 1 (17-19/03): Introdução + Modelos de Ciclo de Vida + Scrum

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 17/03 | Ter | 🟢 | Introdução a Processos de Software + Modelos de Ciclo de Vida (cascata, espiral, V). Apresentação do curso. |
| 19/03 | Qui | 🟢 | Simulação: Sprint Planning com user stories fictícias + Discussão sobre leituras |

**Conteúdo**: Motivação, definições, o paradoxo da produtividade com IA, caso XZ Utils. Waterfall (Royce), Espiral (Boehm), Modelo V, transição para métodos ágeis, Scrum.
**Entregas**: Nenhuma (semana de ambientação)  
**Importante**: Formação dos grupos de projeto até 26/03.

**Leitura 1**: Royce (1970) — *Managing the Development of Large Software Systems* — [PDF](https://www.praxisframework.org/files/royce1970.pdf)  
**Leitura 2**: Boehm (1988) — *A Spiral Model of Software Development and Enhancement* — [PDF](https://www.cse.msu.edu/~cse435/Homework/HW3/boehm.pdf)  
**Leitura 3**: Schwaber & Sutherland (2020) — *Guia do Scrum* (13 pág.) — [PDF (PT-BR)](https://scrumguides.org/docs/scrumguide/v2020/2020-Scrum-Guide-PortugueseBR-3.0.pdf)  
**Leitura 4**: *Manifesto Ágil* + 12 Princípios — [agilemanifesto.org (PT-BR)](https://agilemanifesto.org/iso/ptbr/manifesto.html)

> **Nota**: As leituras 1-4 serão avaliadas no **Quiz 1 (terça 24/03)**. As leituras 1-2 cobrem os modelos clássicos discutidos na aula de 17/03. As leituras 3-4 são sobre Scrum.

---

### Semana 2 (24-26/03): Extreme Programming e Lean

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 22/03 | Dom | 📺 | **Vídeo 2**: XP (práticas técnicas) + Lean Software Development (7 princípios) |
| 24/03 | Ter | 🟢 | **🧩 Quiz 1** (Modelos de ciclo de vida + Scrum + Manifesto Ágil) + Discussão XP e Lean |
| 26/03 | Qui | 🔵 | **Acompanhamento Online** — Sprint 0 (Proposta do projeto) |

**Conteúdo**: XP values/practices, TDD, pair programming, refactoring, CI, Lean (eliminar desperdício, amplificar aprendizado, decidir o mais tarde possível)  
**Entregas**: 🚀 Sprint 0 — Proposta do projeto (vídeo 5min + documento PDF) — até 26/03

**Leitura 1**: Atlassian — *Kanban: A brief introduction* — [atlassian.com](https://www.atlassian.com/agile/kanban)  
**Leitura 2**: Scrum.org — *Limiting WIP in Scrum with Kanban* — [scrum.org](https://www.scrum.org/resources/blog/limiting-work-progress-wip-scrum-kanban-what-when-who-how)

---

### Semana 3 (31/03 - 02/04): Kanban e Fluxo

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 29/03 | Dom | 📺 | **Vídeo 3**: Kanban — visualizar, limitar WIP, gerenciar fluxo. Scrumban e abordagens híbridas |
| 31/03 | Ter | 🟢 | **🧩 Quiz 2** (XP + Lean) + Prática: configurando o quadro Kanban do projeto no GitHub Projects |
| 02/04 | Qui | 🔴 | **Quinta-feira Santa** — Sem aula |

**Conteúdo**: Sistema Kanban, WIP limits, tempo de espera (lead time) vs tempo de ciclo (cycle time), métricas de fluxo, Scrumban  
**Entregas**:  
- 🚀 **Entrega U1** Sprint 0 — até 03/04 (sex)

---

## UNIDADE 2: Práticas Modernas e Medição (Semanas 4-9)

### Semana 4 (07-09/04): DevOps — Cultura e CI/CD

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 06/04 | Dom | 📺 | **Vídeo 4**: DevOps — cultura, princípios, os Três Caminhos. Introdução a CI/CD com GitHub Actions |
| 07/04 | Ter | 🟢 | **🧩 Quiz 3** (Kanban + fluxo) + Prática: criando o primeiro workflow de CI no projeto |
| 09/04 | Qui | 🔵 | **Acompanhamento Online** — Sprint 1 |

**Conteúdo**: DevOps como movimento cultural (CALMS), integração contínua, entrega contínua, deploy contínuo, GitHub Actions  
**Entregas**: 🚀 Sprint 1 (vídeo 8min) — até 10/04 (sex)

**Leitura 1**: Fowler (2024) — *Continuous Integration* — [martinfowler.com](https://martinfowler.com/articles/continuousIntegration.html)  
**Leitura 2**: GitHub Docs — *Quickstart for GitHub Actions* — [docs.github.com](https://docs.github.com/en/actions/get-started/quickstart)

---

### Semana 5 (14-16/04): Containerização e Infraestrutura como Código

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 13/04 | Dom | 📺 | **Vídeo 5**: Docker — containers, imagens, docker-compose. Conceitos de IaC |
| 14/04 | Ter | 🟢 | **🧩 Quiz 4** (DevOps + CI/CD) + Prática: containerizando o projeto da equipe |
| 16/04 | Qui | 🟢 | Prática: docker-compose para desenvolvimento local + portões de qualidade |

**Conteúdo**: Containers vs VMs, Dockerfile, docker-compose, conceitos de IaC, GitOps, portões de qualidade

**Leitura 1**: Docker Docs — *Get Started: Introduction* — [docs.docker.com](https://docs.docker.com/get-started/introduction/)  
**Leitura 2**: Fowler (2016) — *Infrastructure As Code* — [martinfowler.com](https://martinfowler.com/bliki/InfrastructureAsCode.html)

---

### Semana 6 (21-23/04): Métricas DORA e Medição de Desempenho

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 20/04 | Dom | 📺 | **Vídeo 6**: DORA Metrics — as 5 métricas + framework SPACE + 7 arquétipos de equipe |
| 21/04 | Ter | 🔴 | **Tiradentes** — Sem aula |
| 23/04 | Qui | 🔵 | **Acompanhamento Online** — Sprint 2 |

**Conteúdo**: Frequência de implantação, tempo de espera para mudanças, taxa de retrabalho, taxa de falha em mudanças, tempo de recuperação, SPACE framework, os 7 arquétipos DORA 2024  
**Entregas**: 🚀 Sprint 2 (vídeo 8min) — até 24/04 (sex)

**Leitura 1**: DORA Team — *Software Delivery Performance Metrics* — [dora.dev](https://dora.dev/guides/dora-metrics-four-keys/)  
**Leitura 2**: DORA (2024) — *Accelerate State of DevOps Report* (PT-BR) — [PDF](https://dora.dev/research/2024/dora-report/2024-dora-accelerate-state-of-devops-report-ptbr.pdf)  
**Leitura 3**: DORA — *Value Stream Mapping for Software Delivery* — [dora.dev](https://dora.dev/guides/value-stream-management/)  
**Leitura 4**: Atlassian — *What Is Value Stream Mapping?* — [atlassian.com](https://www.atlassian.com/continuous-delivery/principles/value-stream-mapping)

> **Nota**: Sem quiz esta semana (feriado na terça). As leituras 1-4 cobrem DORA + VSM e serão avaliadas no **Quiz 5 (terça 28/04)**.

---

### Semana 7 (28-30/04): Mapeamento de Fluxo de Valor

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 28/04 | Ter | 🟢 | **🧩 Quiz 5** (Containers + IaC + DORA + VSM) + Introdução ao VSM |
| 30/04 | Qui | 🟢 | Workshop: cada equipe mapeia o VSM do seu próprio projeto, identifica gargalos, calcula tempos de espera |

**Conteúdo**: Conceitos de fluxo de valor, mapeamento de estado atual, identificação de desperdícios (muda), estado futuro

**Leitura 1**: Google — *Code Review Developer Guide* — [google.github.io](https://google.github.io/eng-practices/review/)  
**Leitura 2**: Bacchelli & Bird (2013) — *Expectations, Outcomes, and Challenges of Modern Code Review* (ICSE) — [PDF](https://sback.it/publications/icse2013.pdf)

---

### Semana 8 (05-07/05): Revisão e Qualidade de Processos

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 04/05 | Dom | 📺 | **Vídeo 7**: Qualidade de Processos — revisões, inspeções de Fagan, métricas de processo |
| 05/05 | Ter | 🟢 | **🧩 Quiz 6** (Revisão de código) + Revisão geral U1+U2 |
| 07/05 | Qui | 🔵 | **Acompanhamento Online** — Sprint 3 + Revisão para prova |

**Conteúdo**: Revisões e inspeções (Fagan), métricas de processo vs produto, revisão de todo conteúdo U1+U2  
**Entregas**:  
- 🚀 Sprint 3 (vídeo 8min) — até 08/05 (sex)  
- 🚀 **Entrega U2** (Sprints 1-3 + Quiz de Leitura) — até 08/05 (sex)

---

### Semana 9 (12/05): PROVA ESCRITA

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| **12/05** | **Ter** | 📚 | **PROVA ESCRITA — Unidades 1 e 2** (10:30-12:00) |
| 14/05 | Qui | 🟢 | Sem aula — Professor corrigindo provas |

**Conteúdo da Prova**: Todo material das Unidades 1 e 2  
**Formato**: Individual, com consulta a uma folha A4 (frente e verso, manuscrita)

---

## UNIDADE 3: Organizações, IA e Melhoria Contínua (Semanas 10-15)

### Semana 10 (19-21/05): Topologias de Equipe e Design Organizacional

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 18/05 | Dom | 📺 | **Vídeo 8**: Topologias de Equipe — 4 tipos de equipe, 3 modos de interação, Lei de Conway |
| 19/05 | Ter | 🟢 | Exercício: mapear a organização de um case real usando Topologias de Equipe |
| 21/05 | Qui | 🔵 | **Acompanhamento Online** — Sprint 4 + Devolutiva da prova |

**Conteúdo**: Alinhada ao fluxo (stream-aligned), Plataforma, Habilitadora, Subsistema complicado; modos de interação: Colaboração, X-como-Serviço, Facilitação; Lei de Conway e Manobra Inversa de Conway  
**Entregas**:  
- 🚀 Sprint 4 (vídeo 8min) — até 22/05 (sex)

**Leitura 1**: Conway (1968) — *How Do Committees Invent?* — [melconway.com](https://www.melconway.com/research/committees.html)  
**Leitura 2**: Fowler (2023) — *Team Topologies* — [martinfowler.com](https://martinfowler.com/bliki/TeamTopologies.html)

---

### Semana 11 (26-28/05): Engenharia de Plataformas e SRE

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 25/05 | Dom | 📺 | **Vídeo 9**: Engenharia de Plataformas + SRE — SLOs, SLIs, orçamentos de erro |
| 26/05 | Ter | 🟢 | **🧩 Quiz 7** (Topologias de Equipe + Conway) + Discussão sobre plataformas internas |
| 28/05 | Qui | 🔵 | **Acompanhamento Online** — Dúvidas + Progresso dos projetos |

**Conteúdo**: Plataformas Internas de Desenvolvimento, SRE, SLOs/SLIs/orçamentos de erro, observabilidade

**Leitura 1**: Google — *Site Reliability Engineering*, Ch. 1: Introduction — [sre.google](https://sre.google/sre-book/introduction/)  
**Leitura 2**: Microsoft — *Foundations of Platform Engineering: An Introduction* — [learn.microsoft.com](https://learn.microsoft.com/en-us/training/modules/foundations-platform-engineering/)

---

### Semana 12 (02-04/06): IA e Processos de Software

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 01/06 | Dom | 📺 | **Vídeo 10**: O Paradoxo da Produtividade com IA — DORA 2024, estudo METR |
| 02/06 | Ter | 🟢 | **🧩 Quiz 8** (SRE + Engenharia de Plataformas) + Debate sobre IA e processos |
| 04/06 | Qui | 🔴 | **Corpus Christi** — Sem aula |

**Conteúdo**: Paradoxo da Produtividade com IA, 90% de adoção vs métricas estagnadas, impacto em revisão de código, testes, integração; Modelo de Capacidades de IA do DORA; governança de IA em processos

**Leitura 1**: METR (2025) — *Measuring the Impact of AI on Developer Productivity* — [metr.org](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/)  
**Leitura 2**: Brynjolfsson et al. (2018) — *AI and the Modern Productivity Paradox* — [NBER PDF](https://www.nber.org/system/files/working_papers/w24001/w24001.pdf)

---

### Semana 13 (09-11/06): Padrões, Maturidade e Melhoria Contínua

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 08/06 | Dom | 📺 | **Vídeo 11**: CMMI, ISO/IEC 12207, IEEE. Melhoria contínua: kaizen, PDCA |
| 09/06 | Ter | 🟢 | **🧩 Quiz 9** (IA + produtividade) + Atividade: conectando padrões com práticas ágeis |
| 11/06 | Qui | 🔵 | **Acompanhamento Online** — Sprint 5 (final) |

**Conteúdo**: Modelos de maturidade (CMMI V3.0), ISO/IEC 12207:2017, IEEE standards, relação com práticas ágeis modernas, PDCA, kaizen  
**Entregas**: 🚀 Sprint 5 — MVP completo (vídeo 10min) — até 12/06 (sex)

**Leitura 1**: Microsoft — *CMMI: Background Notes* — [learn.microsoft.com](https://learn.microsoft.com/en-us/azure/devops/boards/work-items/guidance/cmmi/guidance-background-to-cmmi?view=azure-devops)  
**Leitura 2**: Humphrey (SEI/CMU) — *The Watts New? Collection* — [PDF](https://www.sei.cmu.edu/documents/1869/2009_003_001_15035.pdf)

---

### Semana 14 (16-18/06): Apresentações Finais

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 16/06 | Ter | 🟢 | **Apresentações finais** (Grupos 1-6) |
| 18/06 | Qui | 🟢 | **Apresentações finais** (Grupos 7-12) |

**Formato**: 12 minutos por equipe + 3 minutos de perguntas (15 min total)  
**Entregas**:
- 🚀 **Entrega U3** (Projeto Final + Proposta de Melhoria de Processo) — até 26/06 (sex)

---

### Semana 15 (23-25/06): Encerramento

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 23/06 | Ter | 🟢 | Retrospectiva geral do curso + Devolutiva |
| 25/06 | Qui | 🔵 | **Acompanhamento Online** — Dúvidas sobre correção e notas |

**Prazo final**: Entrega U3 até 26/06 (sex) às 23:59  
**Consolidação**: Notas no SIGAA até 11/07

---

## Resumo de Entregas

### Sprints do Projeto

| Sprint | Conteúdo | Prazo | Vídeo |
|--------|----------|-------|-------|
| Sprint 0 | Proposta do projeto | 26/03 (qui) | 5 min |
| Sprint 1 | Backlog + primeiras funcionalidades + CI configurado | 10/04 (sex) | 8 min |
| Sprint 2 | Funcionalidades core + Docker + métricas DORA | 24/04 (sex) | 8 min |
| Sprint 3 | Funcionalidades completas + VSM do pipeline | 08/05 (sex) | 8 min |
| Sprint 4 | Refinamento + qualidade + testes | 22/05 (sex) | 8 min |
| Sprint 5 | MVP completo + proposta de melhoria | 12/06 (sex) | 10 min |

### Entregas por Unidade

| Unidade | Prazo | Componentes |
|---------|-------|-------------|
| U1 | 03/04 (sex) | Sprint 0 + Quiz de Leitura |
| U2 | 08/05 (sex) | Sprints 1-3 + Prova (12/05) + Quiz de Leitura |
| U3 | 26/06 (sex) | Sprints 4-5 + Apresentação Final + Proposta de Melhoria |

---

## Feriados e Datas Especiais

| Data | Evento | Impacto |
|------|--------|---------|
| 02/04 | Quinta-feira Santa | Sem aula |
| 21/04 | Tiradentes | Sem aula (feriado na terça, sem quiz) |
| 04/06 | Corpus Christi | Sem aula |

---

## Datas Importantes

| Data | Evento |
|------|--------|
| 26/03 | Prazo para formação de grupos + Sprint 0 |
| 03/04 (sex) | Entrega U1 |
| 08/05 (sex) | Entrega U2 |
| **12/05 (ter)** | **PROVA ESCRITA** |
| 16 e 18/06 | Apresentações finais |
| 26/06 (sex) | Entrega U3 (final) |
| 11/07 | Término do período |

---

## Acompanhamentos Online (Google Meet)

| # | Data | Foco |
|---|------|------|
| 1 | 26/03 | Sprint 0 — Proposta do projeto |
| 2 | 09/04 | Sprint 1 — Backlog + CI |
| 3 | 23/04 | Sprint 2 — Docker + DORA |
| 4 | 07/05 | Sprint 3 — VSM + Revisão para prova |
| 5 | 21/05 | Sprint 4 — Devolutiva da prova + Progresso |
| 6 | 28/05 | Dúvidas + Progresso dos projetos |
| 7 | 11/06 | Sprint 5 — MVP final |
| 8 | 25/06 | Dúvidas sobre correção e notas |

**Horário**: 10:30-12:00 (mesmo horário das aulas presenciais)  
**Formato**: ~10 minutos por equipe para tirar dúvidas e revisar progresso