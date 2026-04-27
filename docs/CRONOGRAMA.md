# Cronograma Detalhado — Processos de Software

## Bacharelado em Engenharia de Software — UFRN/DIMAp

**Período**: 2026.1 (17/03/2026 a 11/07/2026)  
**Horário**: Terças e Quintas, 10:30 às 12:00 (M56)

---

> **⚠️ Atualização 09/04/2026**: Cronograma reorganizado por **sprint** (não mais por semana). Cada sprint tem **objetivo claro** alinhado ao conteúdo teórico. Sprints duram **2 semanas**. Prova adiada para **26/05 (ter)**. Total de **4 sprints** (Sprint 1 a Sprint 4) após a entrega da proposta (Sprint 0).

---

## Legenda

| Símbolo | Significado |
|---------|-------------|
| 📖 | Leitura obrigatória (antes da aula) |
| 🟢 | Aula presencial (discussão + atividade) |
| 🔵 | Acompanhamento online (Google Meet) |
| 🧩 | Quiz no Multiprova (início da aula de terça) |
| 🚀 | Entrega de sprint do projeto |
| 📚 | Prova |
| 🔴 | Feriado/Sem aula |

---

## Visão Geral do Curso por Sprints

| Sprint | Período | Objetivo | Entrega |
|--------|---------|----------|---------|
| **Sprint 0** | 17/03 - 06/04 | Propor o projeto e definir o processo de trabalho | 06/04 (dom) ✓ |
| **Sprint 1** | 14/04 - 24/04 | Estabelecer o fluxo de trabalho e entregar o primeiro incremento | **30/04 (qui)** ⚠️ |
| **Sprint 2** | 25/04 - 08/05 | Automatizar a entrega com DevOps e começar a medir desempenho | **08/05 (sex)** |
| **Sprint 3** | 09/05 - 22/05 | Analisar o fluxo de valor e propor melhorias baseadas em dados | **22/05 (sex)** |
| 📚 **PROVA** | 26/05 (ter) | Avaliação individual dos conceitos de U1+U2 | — |
| **Sprint 4** | 27/05 - 12/06 | Consolidar o MVP e refletir criticamente sobre o processo | **12/06 (sex)** |
| **Apresentações** | 16-18/06 | Defesa final dos projetos | — |
| **Encerramento** | 23-25/06 | Correção, notas, feedback | 26/06 (sex) |

---

## Mapeamento Unidade ↔ Sprint

| Unidade | Sprints | Conteúdo Principal |
|---------|---------|-------------------|
| **U1** | Sprint 0 + Sprint 1 | Fundamentos ágeis (Scrum, XP, Lean, Kanban) |
| **U2** | Sprint 2 + Sprint 3 + Prova | DevOps, DORA, VSM, Qualidade |
| **U3** | Sprint 4 + Apresentações | Team Topologies, SRE, IA, Maturidade |

---

## SPRINT 0 (17/03 - 06/04): Proposta do Projeto ✓

### Objetivo do Sprint

Cada equipe propõe seu projeto, define o produto, forma o backlog inicial e configura o processo de trabalho. É a fundação sobre a qual todos os outros sprints serão construídos.

### Aulas do Sprint

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 17/03 | Ter | 🟢 | Introdução + Modelos de Ciclo de Vida (cascata, espiral, V, iterativo) |
| 19/03 | Qui | 🟢 | Scrum: papéis, cerimônias, artefatos + Simulação de Sprint Planning |
| 24/03 | Ter | 🟢 | Discussão XP e Lean (preparatório para aprofundamento) |
| 26/03 | Qui | 🔵 | **Acompanhamento Online** — Sprint 0 (Proposta do projeto) |
| 31/03 | Ter | 🔴 | ~~Sem aula — professor doente~~ |
| 02/04 | Qui | 🔴 | ~~Quinta-feira Santa~~ |
| 07/04 | Ter | 🟢 | XP e Lean |
| 09/04 | Qui | 🔵 | **Acompanhamento Online** |

### Leituras da Sprint

- **L1**: Royce (1970) — *Managing the Development of Large Software Systems*
- **L2**: Manifesto Ágil — [agilemanifesto.org](https://agilemanifesto.org/iso/ptbr/manifesto.html)
- **L3**: Scrum Guide 2020 — [scrumguides.org](https://scrumguides.org/)

### Entrega do Sprint

🚀 **Sprint 0** — Proposta do projeto (vídeo 5min + documento PDF) — prazo estendido até **06/04 (dom)**

---

## SPRINT 1 (14/04 - 24/04): Estabelecer o Fluxo de Trabalho

### Objetivo do Sprint

A equipe coloca o processo em operação: primeira aplicação prática de Scrum, XP e Kanban no projeto. Ao final do sprint, o time deve ter um **primeiro incremento funcional**, um **quadro Kanban em uso real** com WIP limits, e ter feito **pelo menos uma daily e uma retrospectiva** documentadas.

### Aulas do Sprint

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 14/04 | Ter | 🟢 | Fechamento de Lean (princípios Lean Software + fluxo + pull + gestão visual) + Kanban como método (4 princípios, 6 práticas, **WIP limits**, GitHub Projects) |
| 16/04 | Qui | 🟢 | **🧩 Quiz 2** (XP + Lean + Kanban) + Kanban aplicado ao projeto: revisão dos quadros das equipes + retrospectiva de sprint |
| 21/04 | Ter | 🔴 | **Tiradentes** — Sem aula |
| 23/04 | Qui | 🔵 | **Acompanhamento Online** — Sprint 1 (revisão de projetos, feedback sobre quadros Kanban) |

### Conteúdo Habilitador

- **XP**: práticas técnicas (TDD, pair programming, refatoração, CI), design evolutivo, YAGNI
- **Lean Software Development**: 2 pilares (respeito pelas pessoas + melhoria contínua), 7 princípios Poppendieck, muda/mura/muri
- **Kanban**: 4 princípios, 6 práticas, WIP limits, Lei de Little, lead time vs cycle time, classes de serviço
- **Retrospectivas eficazes**: formatos, técnicas, como evitar teatro

### Leituras da Sprint

- **L4**: Fowler (2004) — *Is Design Dead?* — [martinfowler.com](https://martinfowler.com/articles/designDead.html)
- **L5**: Poppendieck & Poppendieck — *Lean Software Development* (introdução + 7 princípios)
- **L6**: Larman & Vodde — *Lean Primer* (capítulo 1)
- **L7**: Anderson (2010) — *Kanban* (capítulos 1-2)

### Entrega do Sprint

🚀 **Sprint 1** (vídeo 8min + retrospectiva documentada) — prazo estendido até **30/04 (qui)**

**Esperado no vídeo**:
1. Demonstração do primeiro incremento funcional
2. Screenshot do quadro Kanban com WIP limits em uso
3. Evidência de pelo menos 1 daily e 1 retrospectiva
4. Reflexão sobre XP/Lean/Kanban aplicados na prática

---

## SPRINT 2 (25/04 - 08/05): Automatizar a Entrega com DevOps

### Objetivo do Sprint

A equipe introduz automação e medição no projeto: **pipeline CI/CD funcionando**, **Docker para reprodutibilidade** e **primeiras métricas DORA coletadas**. O foco é sair do "funciona na minha máquina" para "entrega contínua com confiança".

### Aulas do Sprint

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 28/04 | Ter | 🟢 | Cultura DevOps: o que é, o que NÃO é, CALMS, CI/CD |
| 30/04 | Qui | 🟢 | **🧩 Quiz 1** (Modelos + Scrum + Manifesto Ágil, **Multiprova 24h**, 25 min) |
| 05/05 | Ter | 🟢 | **🧩 Quiz 3** (DevOps + CI/CD + Docker) + Métricas DORA (5 métricas + SPACE + 7 arquétipos) |
| 07/05 | Qui | 🔵 | **Acompanhamento Online** — Sprint 2 |

### Conteúdo Habilitador

- **DevOps**: cultura CALMS, Três Caminhos (Kim), integração contínua como prática habilitadora
- **CI/CD com GitHub Actions**: workflows, actions, secrets, environments
- **Docker**: imagens, containers, multi-stage builds, docker-compose
- **Infrastructure as Code**: conceitos, GitOps, versionamento de infraestrutura
- **DORA metrics**: frequência de deploy, lead time, change failure rate, time to restore, rework rate, SPACE framework

### Leituras da Sprint

- **L8**: Fowler (2024) — *Continuous Integration* — [martinfowler.com](https://martinfowler.com/articles/continuousIntegration.html)
- **L9**: Kim et al. — *The DevOps Handbook* (capítulos 1-3, no SIGAA)
- **L10**: DORA Team — *Software Delivery Performance Metrics* — [dora.dev](https://dora.dev/guides/dora-metrics-four-keys/)

### Entrega do Sprint

🚀 **Sprint 2** (vídeo 8min + pipeline funcionando + primeiras métricas DORA) — até **08/05 (sex)**

**Esperado no vídeo**:
1. Pipeline de CI/CD funcionando no GitHub Actions (screenshot da aba Actions)
2. Imagem Docker buildada e rodando
3. Primeiras 2-3 métricas DORA coletadas e apresentadas
4. Reflexão sobre o impacto do DevOps no fluxo do time

---

## SPRINT 3 (09/05 - 22/05): Analisar o Fluxo e Propor Melhorias

### Objetivo do Sprint

Com o time já entregando com automação, o foco agora é **análise crítica do processo**: mapear o fluxo de valor (VSM), identificar gargalos e propor melhorias mensuráveis. É o sprint mais reflexivo — conecta teoria a evidências do próprio projeto.

### Aulas do Sprint

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 12/05 | Ter | 🟢 | **🧩 Quiz 5** (VSM + qualidade) + Value Stream Mapping: mapeando o fluxo do próprio projeto |
| 14/05 | Qui | 🟢 | Workshop VSM (continuação): identificar gargalos, calcular lead times, propor melhorias |
| 19/05 | Ter | 🟢 | Controle de qualidade de processos: revisões, inspeções (Fagan), métricas de processo |
| 21/05 | Qui | 🔵 | **Acompanhamento Online** — Sprint 3 + Revisão para a prova |

### Conteúdo Habilitador

- **Value Stream Mapping**: conceitos, diagramação do estado atual, identificação de muda, estado futuro
- **Análise de fluxo**: lead time vs cycle time, tempos em fila, identificação de gargalos
- **Controle de qualidade**: code reviews estruturados, inspeções Fagan, critérios de qualidade
- **Retrospectivas baseadas em dados**: usando métricas DORA + VSM para conduzir melhoria contínua
- **Preparação para prova**: consolidação de U1+U2

### Leituras da Sprint

- **L12**: Martin & Osterling — *Value Stream Mapping* (capítulo 1)
- **L13**: Google — *Code Review Developer Guide* — [google.github.io](https://google.github.io/eng-practices/review/)
- **L14**: Bacchelli & Bird (2013) — *Expectations, Outcomes, and Challenges of Modern Code Review*

### Entrega do Sprint

🚀 **Sprint 3** (vídeo 8min + VSM do estado atual + análise de gargalos) — até **22/05 (sex)**

**Esperado no vídeo**:
1. VSM do pipeline atual do projeto (diagrama)
2. Identificação de pelo menos 2 gargalos com dados
3. Proposta de 1-2 melhorias mensuráveis
4. Evolução das métricas DORA entre Sprint 2 e Sprint 3

---

## PROVA ESCRITA — 26/05 (Terça)

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 26/05 | Ter | 📚 | **PROVA ESCRITA** — Unidades 1 e 2 (10:30-12:00) |
| 28/05 | Qui | 🟢 | Devolutiva da prova + Abertura da U3: Team Topologies (início do Sprint 4) |

**Conteúdo da prova**: Todo material das Unidades 1 e 2 — modelos de ciclo de vida, Scrum, XP, Lean, Kanban, DevOps, CI/CD, Docker, DORA, VSM, controle de qualidade.

**Formato**: Individual, com consulta a **1 folha A4 (frente e verso, manuscrita)**.

---

## SPRINT 4 (27/05 - 12/06): Consolidar e Refletir Criticamente

### Objetivo do Sprint

Último sprint do projeto. A equipe **finaliza o MVP**, produz a **proposta de melhoria de processo** (entregável da U3) e se prepara para as apresentações finais. O conteúdo teórico amplia a discussão para organizações, IA e maturidade.

### Aulas do Sprint

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 28/05 | Qui | 🟢 | Devolutiva da prova + Team Topologies: 4 tipos de equipe, 3 modos de interação, Lei de Conway |
| 02/06 | Ter | 🟢 | **🧩 Quiz 6** (Team Topologies + SRE) + Engenharia de Plataformas e SRE (SLOs, error budgets) |
| 04/06 | Qui | 🔴 | **Corpus Christi** — Sem aula |
| 09/06 | Ter | 🟢 | **🧩 Quiz 7** (IA e processos) + IA e Processos de Software: o Paradoxo da Produtividade (DORA 2025) |
| 11/06 | Qui | 🔵 | **Acompanhamento Online** — Sprint 4 final + preparação de apresentações |

### Conteúdo Habilitador

- **Team Topologies**: stream-aligned, platform, enabling, complicated-subsystem teams; modos de interação; Inverse Conway Maneuver
- **Engenharia de Plataformas e SRE**: Internal Developer Platforms, SLOs, SLIs, error budgets, toil reduction
- **IA e Processos**: Paradoxo da Produtividade, DORA AI Capabilities Model, governança de IA em processos
- **Modelos de maturidade**: CMMI V3.0, ISO/IEC 12207, IEEE standards — relação com práticas modernas

### Leituras da Sprint

- **L15**: Skelton & Pais — *Team Topologies* (capítulos 1-3)
- **L16**: Conway (1968) — *How Do Committees Invent?*
- **L17**: Google SRE Book — *Introducing Site Reliability Engineering* — [sre.google](https://sre.google/sre-book/introduction/)
- **L18**: DORA (2025) — *AI Capabilities Model* (seções sobre IA e processos)

### Entrega do Sprint

🚀 **Sprint 4** (vídeo 10min + MVP completo + proposta de melhoria de processo) — até **12/06 (sex)**

**Esperado no vídeo** (sprint final):
1. MVP completo funcionando
2. Evolução do processo ao longo de todo o semestre (comparação Sprint 1 → Sprint 4)
3. Métricas DORA finais coletadas
4. VSM do estado futuro (melhorias propostas)
5. Reflexão sobre o que a equipe aprendeu sobre processos

---

## APRESENTAÇÕES FINAIS (16-18/06)

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 16/06 | Ter | 🟢 | **Apresentações finais** (parte 1) |
| 18/06 | Qui | 🟢 | **Apresentações finais** (parte 2) |

**Formato**: 12 minutos por equipe + 3 minutos de perguntas (15 min total)  
**Foco**: análise crítica do processo vivido, uso de métricas, reflexão sobre aprendizados

---

## ENCERRAMENTO (23-25/06)

| Data | Dia | Tipo | Atividade |
|------|-----|------|-----------|
| 23/06 | Ter | 🔴 | Sem aula — professor corrigindo trabalhos |
| 25/06 | Qui | 🔵 | **Acompanhamento Online** — Dúvidas sobre correção e notas |

**Prazo final**: Entrega U3 até 26/06 (sex) às 23:59  
**Consolidação**: Notas no SIGAA até 11/07

---

## Resumo de Entregas

### Sprints do Projeto

| Sprint | Objetivo | Prazo | Duração Vídeo |
|--------|----------|-------|---------------|
| Sprint 0 | Proposta do projeto | 06/04 (dom) ✓ | 5 min |
| Sprint 1 | Estabelecer fluxo de trabalho | **24/04 (sex)** | 8 min |
| Sprint 2 | Automatizar entrega com DevOps | **08/05 (sex)** | 8 min |
| Sprint 3 | Analisar fluxo e propor melhorias | **22/05 (sex)** | 8 min |
| Sprint 4 | Consolidar MVP + reflexão crítica | **12/06 (sex)** | 10 min |

### Quizzes (Multiprova)

| Quiz | Conteúdo | Data | Sprint |
|------|----------|------|--------|
| Quiz 1 | Modelos + Scrum + Manifesto | **30/04 (qui)** — Multiprova 24h | Sprint 2 |
| Quiz 2 | XP + Lean + Kanban | 16/04 (qui) | Sprint 1 |
| Quiz 3 | DevOps + CI/CD + Docker | 05/05 (ter) | Sprint 2 |

| Quiz 4 | VSM + qualidade | 12/05 (ter) | Sprint 3 |
| Quiz 5 | Team Topologies + SRE | 02/06 (ter) | Sprint 4 |
| Quiz 6 | IA + processos | 09/06 (ter) | Sprint 4 |

### Entregas por Unidade

| Unidade | Sprints | Prazo Final | Componentes |
|---------|---------|-------------|-------------|
| **U1** | Sprint 0 + Sprint 1 | **24/04 (sex)** | Proposta + primeiro incremento + Quizzes 1-2 |
| **U2** | Sprint 2 + Sprint 3 + Prova | **22/05 (sex)** + 26/05 | CI/CD + DORA + VSM + Prova |
| **U3** | Sprint 4 + Apresentação | **26/06 (sex)** | MVP + proposta de melhoria + defesa final |

---

## Feriados e Datas Especiais

| Data | Evento | Impacto |
|------|--------|---------|
| 02/04 | Quinta-feira Santa | Sem aula (Sprint 0) |
| 21/04 | Tiradentes | Sem aula (Sprint 1) |
| 01/05 | Dia do Trabalho | Sexta — sem aula regular, sem impacto |
| 04/06 | Corpus Christi | Sem aula (Sprint 4) |

---

## Datas Importantes

| Data | Evento |
|------|--------|
| 19/03 | Prazo para formação de grupos |
| **06/04 (dom)** | Entrega Sprint 0 |
| **30/04 (sex)** | Entrega Sprint 1  |
| **08/05 (sex)** | Entrega Sprint 2 |
| **22/05 (sex)** | Entrega Sprint 3 |
| **26/05 (ter)** | **PROVA ESCRITA** |
| **12/06 (sex)** | Entrega Sprint 4 (MVP completo) |
| 16 e 18/06 | Apresentações finais |
| 26/06 (sex) | Entrega U3 (final) |
| 11/07 | Término do período |

---

## Acompanhamentos Online (Google Meet)

Os acompanhamentos acontecem às quintas-feiras, sincronizados com a turma de Web II:

| # | Data | Foco |
|---|------|------|
| 1 | 26/03 | Sprint 0 — Proposta do projeto |
| 2 | 23/04 | Sprint 1 - Primeira versão do projeto |
| 2 | 07/05 | Sprint 2 — Pipeline + DORA |
| 3 | 21/05 | Sprint 3 + Revisão para prova | 
| 4 | 11/06 | Sprint 4 final + preparação de apresentações |
| 5 | 25/06 | Dúvidas sobre correção e notas |

**Horário**: 10:30-12:00 (mesmo horário das aulas presenciais)  
**Formato**: ~10 minutos por equipe para tirar dúvidas e revisar progresso