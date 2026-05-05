# Plano de Curso — Processos de Software

## Bacharelado em Engenharia de Software — UFRN/DIMAp

**Carga Horária**: 60 horas  
**Modalidade**: Presencial com Sala de Aula Invertida  
**Horário**: Terças e Quintas, 10:30 às 12:00 (M56)  
**Período**: 2026.1 (17/03/2026 a 11/07/2026)

---

## Ementa Oficial

Introdução a Processos de Software. Modelos de Ciclo de Vida de Software (cascata, espiral, modelo V, etc). Processos de Software existentes (processo unificado, metodologias ágeis). Modelagem e especificação de processos de software. Análise e medição de processos de software. Controle de qualidade em processos de software (revisões, inspeções, coleta e análise de métricas). Modelos de processos e padrões (IEEE, ISO). Implantação e Melhoria de Processos de Software.

---

## Objetivos

### Objetivo Geral

Capacitar o estudante a compreender, analisar, projetar e melhorar processos de desenvolvimento de software, com ênfase em métodos ágeis, práticas DevOps e medição de desempenho de entrega — preparando-o para atuar como agente de melhoria contínua em organizações de software.

### Objetivos Específicos

Ao final do curso, o estudante será capaz de:

1. Compreender os fundamentos de processos de software e por que eles importam mais do que nunca na era da IA
2. Comparar modelos de ciclo de vida clássicos (cascata, espiral, V) e identificar seus contextos de aplicação
3. Aplicar frameworks ágeis (Scrum, XP, Kanban) em projetos reais com equipes
4. Projetar e operar pipelines de CI/CD usando GitHub Actions e Docker
5. Medir o desempenho de entrega de software usando métricas DORA
6. Realizar Mapeamento de Fluxo de Valor (Value Stream Mapping) para identificar gargalos
7. Compreender princípios de Engenharia de Plataformas e Topologias de Equipe (Team Topologies)
8. Avaliar criticamente o impacto de ferramentas de IA em processos de software
9. Aplicar frameworks de melhoria contínua (kaizen, retrospectivas baseadas em dados, PDCA)
10. Conhecer modelos de maturidade e padrões (CMMI, ISO/IEC 12207, IEEE) e sua relação com práticas modernas

---

## Abordagem Pedagógica

### Filosofia do Curso

Este curso adota uma perspectiva **ágil-primeiro**: os métodos ágeis não são apresentados como alternativa aos modelos clássicos, mas como lente principal para entender processos de software modernos. Modelos clássicos são estudados como contexto histórico e para compreensão de domínios regulados nos quais ainda se aplicam.

O curso é fortemente influenciado pelo **DORA Report 2025**, que demonstra que o design de processos é a competência diferenciadora na era da IA — pois sem processos bem projetados, ganhos de produtividade individuais não se traduzem em desempenho organizacional.

### Sala de Aula Invertida (Flipped Classroom)

```
📖 ANTES DA AULA (em casa)
   └── Faça as leituras da sprint (artigos, guias, documentação)
   └── Anote dúvidas

🏫 TERÇA-FEIRA (presencial, 10:30-12:00)
   └── 🧩 Quiz no Multiprova sobre as leituras (10-15 min)
   └── Revisão rápida + Esclarecimento de dúvidas
   └── Atividade prática ou discussão guiada

🏫 QUINTA-FEIRA (presencial ou online)
   └── Continuação da prática / Discussão aprofundada
   └── Acompanhamento de projeto (via Google Meet, a cada final de sprint)
```

Todos os materiais de leitura são **gratuitos e abertos**: artigos científicos, guias oficiais (Scrum Guide, DORA Report), documentação de referência (Docker, GitHub Actions), e blog posts de autores reconhecidos (Martin Fowler, Google Engineering). Detalhes completos no [Cronograma](CRONOGRAMA.md).

### Aprendizagem Baseada em Projetos (Project-Based Learning) com Scrum

O curso é centrado no desenvolvimento de um **projeto integrador** organizado em sprints, onde as equipes vivenciam na prática os processos que estudam em teoria:

- **Equipes de 3-4 estudantes** (já formadas)
- **4 sprints de 2 semanas** (Sprint 1 a Sprint 4) após a proposta inicial (Sprint 0)
- **Cada sprint com objetivo claro** alinhado ao conteúdo teórico da disciplina
- **Acompanhamento online** ao final de cada sprint via Google Meet
- **Avaliação por vídeo** gravado pela equipe + peer evaluation

### O que torna este curso diferente

1. **Medição real**: equipes coletam métricas DORA do próprio projeto desde o Sprint 1
2. **Value Stream Mapping**: exercício prático de mapeamento do próprio pipeline de entrega
3. **IA como objeto de estudo**: análise crítica de como ferramentas de IA impactam processos
4. **Retrospectivas baseadas em dados**: decisões de melhoria fundamentadas em métricas, não em opiniões
5. **Processo como produto**: artefatos de processo (backlog, gráfico de burndown, VSM) são entregáveis avaliados

---

## Conteúdo Programático por Sprint

> **Atualização 09/04/2026**: O conteúdo teórico do curso está organizado por **sprint** do projeto, de modo que cada bloco de teoria habilite uma capacidade prática que a equipe aplicará no sprint correspondente.
>
> **Atualização 05/05/2026**: Datas ajustadas para reposição de aulas não realizadas (03/03, 05/03, 10/03, 12/03, 31/03, 28/04 e 30/04). Prova adiada para **02/06 (ter)**. Apresentações finais adiadas para **30/06 (ter) e 02/07 (qui)**.

### Sprint 0 (17/03 - 06/04): Proposta do Projeto

**Objetivo**: Propor o projeto e definir o processo de trabalho.

| Tópico |
|--------|
| Introdução a Processos de Software + Modelos de Ciclo de Vida |
| Scrum — framework, papéis, cerimônias, artefatos |
| Extreme Programming e Lean Software Development (visão geral) |

### Sprint 1 (14/04 - 24/04): Estabelecer o Fluxo de Trabalho

**Objetivo**: Primeira aplicação prática de Scrum + XP + Kanban no projeto.

| Tópico |
|--------|
| XP em profundidade: práticas técnicas e design evolutivo |
| Lean Software Development: 7 princípios e eliminação de desperdício |
| Kanban, fluxo e sistemas puxados (WIP limits, Lei de Little) |
| Retrospectivas eficazes |

### Sprint 2 (05/05 - 19/05): Automatizar a Entrega com DevOps

**Objetivo**: Introduzir CI/CD, containers e métricas DORA no projeto.

| Tópico |
|--------|
| DevOps — cultura, princípios (CALMS, Três Caminhos) |
| CI/CD com GitHub Actions na prática |
| Containerização com Docker e Infrastructure as Code |
| Métricas DORA (5 métricas) + SPACE framework + 7 arquétipos |

### Sprint 3 (20/05 - 02/06): Analisar o Fluxo e Propor Melhorias

**Objetivo**: Mapear o fluxo de valor (VSM) e propor melhorias baseadas em dados.

| Tópico |
|--------|
| Value Stream Mapping — mapeando e melhorando o fluxo |
| Controle de qualidade: revisões, inspeções (Fagan), métricas de processo |
| Retrospectivas baseadas em dados |
| Revisão e preparação para prova |

### PROVA ESCRITA — 02/06 (ter)

Avaliação individual de todo o conteúdo de U1 + U2.

### Sprint 4 (03/06 - 19/06): Consolidar e Refletir Criticamente

**Objetivo**: Finalizar o MVP e produzir a proposta de melhoria de processo.

| Tópico |
|--------|
| Team Topologies e design organizacional |
| Engenharia de Plataformas e SRE |
| IA e Processos de Software — o Paradoxo da Produtividade |
| Padrões e modelos de maturidade (CMMI, ISO, IEEE) + Melhoria contínua |

### Apresentações Finais (30/06 e 02/07)

Defesa dos projetos com foco em análise crítica do processo vivido.

---

## Mapeamento Unidade ↔ Sprint

| Unidade | Sprints | Conteúdo Principal |
|---------|---------|-------------------|
| **U1** | Sprint 0 + Sprint 1 | Fundamentos ágeis (Scrum, XP, Lean, Kanban) |
| **U2** | Sprint 2 + Sprint 3 + Prova | DevOps, DORA, VSM, Qualidade |
| **U3** | Sprint 4 + Apresentações | Team Topologies, SRE, IA, Maturidade |

---

## Avaliação

A nota final é a **média aritmética das 3 unidades**:

```
Nota Final = (U1 + U2 + U3) / 3
```

### Resumo por Unidade

| Unidade | Componentes |
|---------|-------------|
| **U1** | Sprint 0 (70%) + Participação (30%) |
| **U2** | **Prova Escrita (40%)** + Sprints 1-3 (40%) + Participação (20%) |
| **U3** | Projeto Final (60%) + Proposta de Melhoria de Processo (25%) + Participação (15%) |

Detalhes completos em [docs/AVALIACAO.md](AVALIACAO.md).

---

## Ferramentas

| Ferramenta | Uso |
|------------|-----|
| **GitHub** | Repositórios de projeto, GitHub Projects (Kanban/Scrum board) |
| **GitHub Actions** | Pipelines de CI/CD |
| **Docker** | Containerização |
| **Multiprova** | Quizzes de leitura |
| **Discord** | Comunicação da turma |
| **Google Meet** | Acompanhamentos online de projeto |
| **SIGAA** | Entregas oficiais e notas |

---

## Referências

### Livros-Texto Abertos (acesso gratuito)

- **VALENTE, Marco Tulio.** *Engenharia de Software Moderna.* UFMG, 2020. Disponível em: [engsoftmoderna.info](https://engsoftmoderna.info/) (PT-BR)
- **LETAW, Lara.** *Handbook of Software Engineering Methods.* 2nd ed. Oregon State University, 2024. CC BY-NC 4.0. Disponível em: [open.oregonstate.education/setextbook](https://open.oregonstate.education/setextbook/)
- **BEYER, Betsy et al.** *Site Reliability Engineering.* Google/O'Reilly, 2017. Disponível em: [sre.google/sre-book](https://sre.google/sre-book/table-of-contents/)
- **IEEE Computer Society.** *SWEBOK Guide V4.0.* 2024. Disponível em: [computer.org/swebok](https://www.computer.org/education/bodies-of-knowledge/software-engineering/v4)

### Guias e Documentos Oficiais (acesso gratuito)

- **SCHWABER, Ken; SUTHERLAND, Jeff.** *Guia do Scrum 2020.* Disponível em: [scrumguides.org (PT-BR)](https://scrumguides.org/docs/scrumguide/v2020/2020-Scrum-Guide-PortugueseBR-3.0.pdf)
- **BECK, Kent et al.** *Manifesto Ágil.* 2001. Disponível em: [agilemanifesto.org (PT-BR)](https://agilemanifesto.org/iso/ptbr/manifesto.html)
- **DORA Team.** *Accelerate State of DevOps Report 2025.* Google Cloud. Disponível em: [dora.dev](https://dora.dev/)

### Artigos Seminais (acesso aberto)

- **ROYCE, Winston W.** Managing the Development of Large Software Systems. 1970. [PDF](https://www.praxisframework.org/files/royce1970.pdf)
- **BOEHM, Barry W.** A Spiral Model of Software Development and Enhancement. IEEE Computer, 1988. [PDF](https://www.cse.msu.edu/~cse435/Homework/HW3/boehm.pdf)
- **CONWAY, Melvin E.** How Do Committees Invent? 1968. [melconway.com](https://www.melconway.com/research/committees.html)
- **BACCHELLI, Alberto; BIRD, Christian.** Expectations, Outcomes, and Challenges of Modern Code Review. ICSE, 2013. [PDF](https://sback.it/publications/icse2013.pdf)
- **BRYNJOLFSSON, Erik et al.** AI and the Modern Productivity Paradox. NBER, 2018. [PDF](https://www.nber.org/system/files/working_papers/w24001/w24001.pdf)

### Artigos e Blog Posts de Referência

- **FOWLER, Martin.** *Continuous Integration* (2024), *Is Design Dead?* (2004), *Team Topologies* (2023). Disponíveis em: [martinfowler.com](https://martinfowler.com/)
- **Google Engineering.** *Code Review Developer Guide.* Disponível em: [google.github.io/eng-practices](https://google.github.io/eng-practices/review/)
- **DORA.** Guias sobre métricas e VSM. Disponível em: [dora.dev/guides](https://dora.dev/guides/)

### Padrões e Modelos

- IEEE/ISO/IEC 12207:2017 — Software Life Cycle Processes
- CMMI V3.0 — Capability Maturity Model Integration
- ACM/IEEE/AAAI CS2023 — Computer Science Curricula

> **Nota**: Todas as leituras obrigatórias de cada sprint são de acesso gratuito e estão listadas no [Cronograma](CRONOGRAMA.md). Não é necessário comprar nenhum livro para cursar esta disciplina.

---

## Licença

Este material é disponibilizado sob a licença [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).

Você pode compartilhar e adaptar este material para fins não comerciais, desde que atribua crédito e distribua sob a mesma licença.