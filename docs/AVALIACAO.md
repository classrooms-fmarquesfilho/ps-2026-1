# Avaliação — Processos de Software

## Bacharelado em Engenharia de Software — UFRN/DIMAp

**Período**: 2026.1  
**Prof. Fernando Figueira**

> **⚠️ Atualização 05/05/2026**: Datas ajustadas para reposição de aulas não realizadas. Prova adiada para **02/06 (ter)**. Apresentações finais adiadas para **30/06 (ter) e 02/07 (qui)**. Entrega U3 passa a ser **04/07 (sex)**.
>
> **⚠️ Atualização 25/05/2026**:
> - **Sprint 3** com prazo prorrogado para **11/06 (qui)**.
> - **Sprint 4** mesclada com a Apresentação Final em um único entregável: o **Vídeo Final**, com prazo **30/06 (ter) às 23:59** (substitui a apresentação presencial).
> - **Participação removida** como componente avaliativo nas três unidades. Permanece como requisito de aprovação a frequência mínima de 75%.
> - **Pesos redistribuídos** nas três unidades. Os componentes passam a ser:
>   - **U1**: Sprint 0 (50%) + Sprint 1 (40%) + Quiz 2 (10%)
>   - **U2**: Prova (25%) + Sprint 2 (30%) + Sprint 3 (30%) + Quiz 1 (5%) + Quiz 3 (5%) + Quiz 4 (5%)
>   - **U3**: Prova (50%) + Vídeo Final (30%) + Proposta de Melhoria (20%)
> - A **Sprint 1** passa a contar apenas em U1 (deixa de pesar em U2). A **Prova** continua sendo uma única prova realizada em 02/06, com pesos diferentes em U2 (25%) e U3 (50%).
>
> **⚠️ Atualização 06/06/2026**:
> - A **Prova foi adiada para 11/06 (qui)** e passa a ser aplicada no **Multiprova**. Pesos mantidos: 25% da U2 e 50% da U3.
> - A **aula de 02/06 foi cancelada**; o conteúdo de **controle de qualidade** fica por conta das leituras L13/L14 e não é foco da prova.
> - A **Sprint 3 ocorre junto à Entrega Final do Projeto**, a ser entregue em **23/06 (ter)**. Não há mais vídeo separado de Sprint 3: a mesma entrega final é avaliada como **Sprint 3 (30% da U2)** e como **Vídeo Final (30%) + Proposta de Melhoria (20%) da U3** — os pesos das duas unidades recaem sobre o mesmo conjunto de entregáveis.

---

## Estrutura Geral

A avaliação é organizada em **3 unidades** com pesos iguais. A nota final é a média aritmética das três unidades:

```
Nota Final = (U1 + U2 + U3) / 3
```

### Filosofia de Avaliação

Diferente de cursos tradicionais, a avaliação nesta disciplina **enfatiza o projeto e a prática de processos**. Não há listas de exercícios com correção automática — o aprendizado é demonstrado através da vivência do processo, da qualidade dos artefatos produzidos e da capacidade de reflexão crítica sobre a prática.

A avaliação combina três dimensões:

1. **Processo vivido** (sprints, cerimônias, artefatos) — o que a equipe faz
2. **Reflexão crítica** (proposta de melhoria, retrospectivas) — o que a equipe aprende
3. **Conhecimento individual** (prova, quizzes) — o que cada pessoa entende

### Tipos de Avaliação

| Tipo | Componentes | Descrição |
|------|-------------|-----------|
| **Individual** | Prova, Quizzes | Trabalho e conhecimento próprio |
| **Em grupo** | Sprints, Vídeo Final, Proposta de Melhoria | Equipes de 3-4 pessoas |

> **Importante**: O **projeto é em grupo**, mas a contribuição individual de cada membro é avaliada através de commits, presença nos vídeos e capacidade de responder perguntas sobre o processo da equipe.

---

## Calendário de Entregas

> Todas as datas de entrega do curso estão consolidadas aqui.  
> Prazos encerram às **23:59** do dia indicado.

### Sprints do Projeto (Grupo)

| Sprint | Conteúdo | Prazo | Vídeo |
|--------|----------|-------|-------|
| Sprint 0 | Proposta do projeto | 06/04 (dom) ✓ | 5 min |
| Sprint 1 | Estabelecer fluxo de trabalho (Scrum + XP + Kanban aplicados) | 30/04 (qui) ✓ | 8 min |
| Sprint 2 | Automatizar entrega com DevOps (CI/CD + Docker + primeiras métricas DORA) | 19/05 (ter) ✓ | 8 min |
| Sprint 3 | Analisar fluxo e propor melhorias (VSM + métricas + qualidade) — Entrega Final | **23/06 (ter)** | — |
| **🎥 Vídeo** | MVP completo + reflexão crítica final (mescla Sprint 3 + Sprint 4 + apresentação) | **23/06 (ter)** | 12 min |

### Datas Especiais

| Evento | Data | Observação |
|--------|------|------------|
| **Prova (Multiprova)** | **11/06 (qui)** | Laboratório, 10:30-12:00 |
| **Vídeo Final + Proposta de Melhoria** | **23/06 (ter)** | Substitui apresentação presencial |
| Consolidação SIGAA | 11/07 | Término oficial do período |

### Consolidação por Unidade

| Unidade | Período | Entrega Final |
|---------|---------|---------------|
| U1 | 17/03 a 30/04 | 30/04 (qui) ✓ |
| U2 | 05/05 a 23/06 | **23/06 (ter)** + Prova 11/06 |
| U3 | 12/06 a 23/06 | **23/06 (ter)** |

---

## Resumo por Unidade

| Unidade | Componentes | Tipo |
|---------|-------------|------|
| **U1** | Sprint 0 (50%) + Sprint 1 (40%) + Quiz 2 (10%) | Grupo + Individual |
| **U2** | Prova (25%) + Sprint 2 (30%) + Sprint 3 (30%) + Quizzes 1, 3 e 4 (5% cada) | Individual + Grupo + Individual |
| **U3** | **Prova (50%)** + Vídeo Final (30%) + Proposta de Melhoria (20%) | Individual + Grupo + Grupo |

---

## Unidade 1 (Sprint 0 + Sprint 1 + Quiz 2) ✓

### Componentes e Pesos

| Componente | Peso | Tipo | Descrição |
|------------|------|------|-----------|
| Sprint 0 | 50% | Grupo | Proposta do projeto (vídeo 5min + documento) |
| Sprint 1 | 40% | Grupo | Primeiro incremento + Scrum/XP/Kanban aplicados (vídeo 8min) |
| Quiz 2 | 10% | Individual | XP + Lean + Kanban — aplicado em 16/04 (Multiprova) |

### Fórmula

```
U1 = (Sprint0 × 0.50) + (Sprint1 × 0.40) + (Quiz2 × 0.10)
```

> Mudança 25/05: a Sprint 1 passa a contar **em U1** (antes contava apenas como parte do bloco "Sprints 1-3" em U2). O Quiz 2 agora compõe a nota de U1.

---

## Unidade 2 (Sprint 2 + Sprint 3 + Prova)

### Componentes e Pesos

| Componente | Peso | Tipo | Descrição |
|------------|------|------|-----------|
| Prova | 25% | Individual | Em sala (02/06), consulta a 1 folha A4 |
| Sprint 2 | 30% | Grupo | DevOps + CI/CD + Docker + DORA (vídeo 8min) |
| Sprint 3 | 30% | Grupo | VSM + qualidade + análise de gargalos (vídeo 8min) |
| Quiz 1 | 5% | Individual | Modelos + Scrum + Manifesto — aplicado em 07/05 (Multiprova) |
| Quiz 3 | 5% | Individual | DevOps + CI/CD + Docker — aplicado em 12/05 (Multiprova) |
| Quiz 4 | 5% | Individual | VSM + qualidade — aplicado em 26/05 (Multiprova) |

### Fórmula

```
U2 = (Prova × 0.25)
   + (Sprint2 × 0.30) + (Sprint3 × 0.30)
   + (Quiz1 × 0.05) + (Quiz3 × 0.05) + (Quiz4 × 0.05)
```

> Mudança 25/05: a **Prova** vale agora 25% de U2. Cada sprint de U2 vale 30% (Sprint 1 saiu para U1). Os três quizzes de U2 (Quiz 1, 3 e 4) entram com 5% cada.
>
> Mudança 06/06: a **Sprint 3 deixa de ter vídeo próprio** e é entregue dentro da **Entrega Final do Projeto (23/06)**.

---

## Unidade 3 (Vídeo Final + Proposta de Melhoria)

### Componentes e Pesos

| Componente | Peso | Tipo | Descrição |
|------------|------|------|-----------|
| **Prova** | **50%** | Individual | Mesma prova realizada em 11/06 (vale 50% de U3) |
| Vídeo Final | 30% | Grupo | MVP + reflexão crítica do processo (mescla Sprint 4 + Apresentação) |
| Proposta de Melhoria de Processo | 20% | Grupo | Documento VSM + análise DORA + recomendações |

### Fórmula

```
U3 = (Prova × 0.50) + (VídeoFinal × 0.30) + (Proposta × 0.20)
```


---

## Prova (25% da U2 + 50% da U3)

### Informações Gerais

- **Data**: 11/06/2026 (Quinta-feira)
- **Horário**: 10:30 às 12:00
- **Local**: Laboratório A305 (IMD)
- **Duração**: 1h30min
- **Formato**: Individual no Multiprova, consulta permitida a **1 folha A4 (frente e verso, manuscrita)**

### Conteúdo

Todo o material das **Unidades 1 e 2**:

- Fundamentos de processos de software
- Modelos de ciclo de vida (cascata, espiral, V, iterativo)
- Scrum (papéis, cerimônias, artefatos)
- Extreme Programming (valores e práticas)
- Lean Software Development (7 princípios)
- Kanban (princípios, métricas de fluxo)
- DevOps (cultura, CI/CD, containerização)
- Métricas DORA (5 métricas, arquétipos)

> Nota: **Value Stream Mapping (VSM) e controle de qualidade estão excluídos da prova** — os alunos não tiveram tempo de praticar esses conceitos. VSM continua sendo cobrado no projeto (Sprint 3/Entrega Final); controle de qualidade fica nas leituras L13/L14. A prova abrange os demais tópicos das unidades 1 e 2 (modelos de ciclo de vida, Scrum, XP, Lean, Kanban, DevOps, CI/CD, Docker, DORA).

### Formato da Prova

A prova combina questões de diferentes tipos:

1. **Questões conceituais** (30%) — Definições, comparações, análise de cenários
2. **Questões aplicadas** (40%) — Dado um cenário, projetar/melhorar um processo
3. **Questões de análise** (30%) — Interpretar métricas, diagnosticar problemas de processo

### Preparação

- Revise os vídeos semanais e as atividades práticas
- Prepare sua folha de consulta com cuidado (o ato de preparar já é uma forma de estudo)
- Pratique a análise de cenários de processo
- Estude os frameworks (Scrum, XP, Kanban) em profundidade

---

## Projeto Integrador

### Sprint 0: Proposta do Projeto

O Sprint 0 é a **fase de planejamento** onde a equipe define o que será construído e como o processo será organizado.

#### Entregáveis do Sprint 0

1. **Vídeo de apresentação** (5 minutos)
2. **Documento de proposta** (PDF, 3-4 páginas)
3. **Quadro Kanban** configurado no GitHub Projects

#### Sobre o Projeto

O projeto desta disciplina é diferente de projetos de cursos de programação: aqui, **o processo é tão importante quanto o produto**. A equipe deve desenvolver um software funcional, mas será avaliada principalmente pela qualidade com que gerencia seu processo de desenvolvimento.

**O que pode ser o projeto:**
- Uma aplicação web (frontend + backend simples)
- Um aplicativo mobile
- Uma ferramenta CLI útil
- Uma biblioteca ou framework
- Uma contribuição a um projeto open source existente

**Stack tecnológico**: livre (pode usar qualquer linguagem/framework). O importante é que o projeto permita demonstrar práticas de processo (CI/CD, testes, revisão de código, etc).

> **Nota**: Alunos que cursam simultaneamente Web II podem usar o **mesmo projeto** em ambas as disciplinas, desde que os entregáveis sejam distintos. O vídeo de sprint de Processos deve focar no **processo** (como a equipe trabalhou, métricas, retrospectiva), enquanto o de Web foca no **produto** (funcionalidades, código, arquitetura).

---

#### Visão do Produto

**Template obrigatório:**

```
Para [usuários-alvo]
Que [problema/necessidade]
O [nome do produto] é um [categoria do produto]
Que [benefício principal/capacidade]
Diferente de [alternativa existente]
Nosso produto [diferencial único]
```

---

#### Backlog do Produto (Product Backlog)

O backlog deve estar no **GitHub Projects** da equipe, usando formato Kanban com colunas:

- **Backlog** — itens priorizados mas não planejados para o sprint atual
- **Sprint Backlog** — itens do sprint corrente
- **In Progress** — em desenvolvimento
- **In Review** — aguardando revisão de código
- **Done** — concluído (atende ao Definição de Pronto)

Use formato de História de Usuário (User Story): "Como [papel], quero [ação] para [benefício]"

---

#### Estrutura do Vídeo de Sprint 0 (5 minutos)

```
1. Apresentação da Equipe (30s)
   - Nome da equipe e do projeto
   - Integrantes e papéis

2. Visão do Produto (1min30s)
   - Problema que resolve
   - Público-alvo
   - Proposta de valor

3. Definição do MVP (1min30s)
   - Funcionalidades essenciais
   - O que NÃO está no MVP
   - Critérios de sucesso

4. Processo da Equipe (1min30s)
   - Stack tecnológico e justificativa
   - Cadência de sprints e cerimônias planejadas
   - Quadro Kanban configurado
   - Como a equipe vai se comunicar e colaborar
```

---

#### Documento de Proposta (PDF, 3-4 páginas)

1. **Visão do Produto** (usando o template)
2. **Definição do MVP** (funcionalidades dentro e fora do escopo)
3. **Product Backlog** inicial (user stories priorizadas)
4. **Stack Tecnológico** (com justificativas)
5. **Acordo de Processo** (cadência de sprints, cerimônias, ferramentas, Definition of Done)
6. **Equipe** (nome, matrícula, papel de cada integrante)
7. **Link do repositório** e do quadro GitHub Projects

---

#### Critérios de Avaliação do Sprint 0

| Critério | Peso | Descrição |
|----------|------|-----------|
| Clareza da visão | 20% | Problema e solução bem definidos |
| Escopo do MVP | 20% | Funcionalidades realistas e priorizadas |
| Acordo de processo | 25% | Cadência, cerimônias, DoD, ferramentas bem definidos |
| Organização da equipe | 20% | Papéis claros, quadro Kanban configurado |
| Qualidade do vídeo | 15% | Comunicação clara, todos participam, respeita o tempo |

---

### Sprints 1-3: Desenvolvimento (8min cada)

#### Critérios de Avaliação

| Critério | Peso | Descrição |
|----------|------|-----------|
| Funcionalidade implementada | 20% | Software funcionando, incremento visível |
| **Qualidade do processo** | **30%** | Cerimônias realizadas, backlog atualizado, gráfico de queima (burndown), DoD satisfeito |
| CI/CD e práticas técnicas | 20% | Pipeline funcionando, revisão de código, testes |
| Retrospectiva e melhoria | 15% | Identificação de problemas e ações concretas de melhoria |
| Comunicação | 15% | Vídeo claro, todos participam |

> **Nota**: A maior mudança em relação a cursos de programação é que **30% da nota do sprint avalia a qualidade do processo**, não do produto. A equipe deve mostrar no vídeo: como planejou o sprint, como acompanhou o progresso, como fez retrospectiva, e o que mudou de um sprint para o outro.

#### Estrutura do Vídeo de Sprint (8 minutos)

```
1. Objetivo do Sprint (30s)
   - O que foi planejado
   - Relação com o sprint anterior

2. Demonstração (2min)
   - Funcionalidades implementadas
   - Software funcionando

3. Processo (3min) ← FOCO PRINCIPAL
   - Sprint planning: como priorizaram
   - Quadro Kanban: estado atual
   - Burndown/vazão (throughput): como o trabalho fluiu
   - Revisões de código realizadas
   - Pipeline de CI/CD funcionando
   - Métricas coletadas (DORA se aplicável)

4. Retrospectiva (1min30s)
   - O que funcionou bem no processo
   - O que precisa melhorar
   - Ações concretas para o próximo sprint

5. Próximos Passos (1min)
   - Planejamento do próximo sprint
```

---

## Vídeo Final (30% da U3)

### Descrição

O Vídeo Final é a apresentação sobre a última evolução do projeto. Ele substitui a **Sprint 3** (VSM + análise de gargalos + qualidade), a antiga Sprint 4 e a antiga apresentação presencial — todas unificadas em um único vídeo de 12 minutos, entregue em **23/06** junto à Proposta de Melhoria. Como inclui os resultados da Sprint 3, o vídeo deve evidenciar o VSM do pipeline, os gargalos identificados e a evolução das métricas DORA.

### Informações Gerais

- **Prazo**: **23/06/2026 (terça) às 23:59**
- **Formato**: Vídeo gravado (link YouTube/Drive acessível)
- **Duração**: **12 minutos**

### Estrutura Sugerida (12 minutos)

```
1. Introdução (1min)
   - Equipe e projeto
   - Problema que resolve

2. Demonstração do MVP (3min)
   - Funcionalidades principais funcionando
   - Fluxos completos

3. O Processo da Equipe (5min) ← FOCO PRINCIPAL
   - Como o processo evoluiu ao longo do semestre
   - Quadro Kanban: estado final
   - Value Stream Map do pipeline de entrega
   - Métricas DORA coletadas (com gráficos)
   - Principais decisões de processo e seus impactos
   - O que mudou entre Sprint 1 e o fim do semestre
   - Conexão com os conceitos finais (Team Topologies, IA em processos)

4. Lições Aprendidas (2min)
   - O que funcionou e o que não funcionou
   - O que fariam diferente
   - Conexão com os conceitos do curso

5. Conclusão (1min)
   - Resumo das contribuições e aprendizados
```

### Critérios de Avaliação do Vídeo Final

| Critério | Peso | Descrição |
|----------|------|-----------|
| **Análise de processo** | **35%** | Qualidade da reflexão sobre o processo vivido, uso de métricas |
| Demonstração do MVP | 20% | Software funcionando |
| Evolução demonstrada (Sprint 1 → fim) | 15% | Mostra mudança concreta de práticas e métricas |
| Comunicação | 15% | Clareza, domínio do conteúdo, participação de todos |
| Organização | 10% | Respeito ao tempo, estrutura do vídeo, edição |
| Aplicação dos conceitos finais | 5% | Team Topologies, IA em processos — onde se conectam à equipe |

### Dicas de Preparação

1. **Ensaie com timer** — 12 minutos passam rápido
2. **Edite o vídeo** — corte pausas muito longas, mantenha o ritmo
3. **Divida as falas** — é positivo que todos os membros participem
4. **Reaproveite material** — métricas, VSMs e screenshots das sprints anteriores
5. **Teste antes de enviar** — verifique que o arquivo abre e tem áudio

---

## Proposta de Melhoria de Processo (20% da U3)

### Descrição

Cada equipe deve produzir um **documento de análise e proposta de melhoria** do processo que vivenciaram durante o semestre. Este é o entregável que conecta teoria e prática de forma mais direta.

### Estrutura do Documento (PDF, 4-6 páginas)

1. **Value Stream Map — Estado Atual** (1 página)
   - Diagrama do fluxo de valor da equipe (do commit ao "done")
   - Tempos de espera e tempos de processamento em cada etapa
   - Gargalos identificados

2. **Métricas DORA Coletadas** (1 página)
   - Frequência de deploy
   - Tempo de espera (lead time) para mudanças
   - Taxa de falha de mudanças
   - Tempo de recuperação
   - Em qual arquétipo DORA 2025 a equipe se encaixa

3. **Análise de Problemas** (1-2 páginas)
   - Principais desperdícios identificados (usando categorias Lean)
   - Retrospectivas: padrões recorrentes de problemas
   - Análise de causa raiz (5 Whys ou Ishikawa) para pelo menos 1 problema

4. **Value Stream Map — Estado Futuro** (1 página)
   - Proposta de melhoria com base na análise
   - Ações concretas e priorizadas
   - Métricas-alvo (que melhorias de DORA a equipe espera)

5. **Reflexão** (0,5-1 página)
   - Conexão com os conceitos do curso (quais frameworks/princípios informaram as melhorias)
   - O que a equipe aprendeu sobre melhoria de processos

### Prazo

Entrega junto ao Vídeo Final, **23/06 (ter) às 23:59**.

### Critérios de Avaliação

| Critério | Peso |
|----------|------|
| Qualidade do VSM (estado atual e futuro) | 30% |
| Uso adequado de métricas DORA | 25% |
| Profundidade da análise de problemas | 25% |
| Viabilidade e concretude das propostas | 20% |

---

## Frequência

- **Mínimo**: 75% de presença para aprovação
- **Justificativas**: Via SIGAA até 48h após a falta
- **Aulas online**: Presença verificada via Google Meet

---

## Formação de Grupos

### Requisitos

- **Tamanho**: 3 a 4 pessoas
- **Formação**: Até 26/03/2026

> **Dica para quem cursa Web II simultaneamente**: Forme o mesmo grupo em ambas as disciplinas. Você pode usar o mesmo projeto, desde que os entregáveis de cada disciplina sejam distintos (processo vs produto).

---

## Estrutura de Entrega

### Entregas de Unidade (SIGAA)

#### U1: Entregue ✓

#### U2: Entrega até 23/06 (Sprint 3) + Prova em 11/06

```
equipe-nome-u2.zip
├── README.md                    # Links e informações
├── sprints/
│   ├── sprint-1-video.txt       # Link do vídeo Sprint 1
│   ├── sprint-2-video.txt       # Link do vídeo Sprint 2
│   └── sprint-3-video.txt       # Link do vídeo Sprint 3
└── projeto/
    └── repo-link.txt            # Link do repositório
```

#### U3: Entrega Final até 23/06

```
equipe-nome-final.zip
├── README.md                    # Resumo e links
├── video-final/
│   └── video-link.txt           # Link do Vídeo Final (12min)
├── projeto/
│   └── repo-link.txt            # Link do repositório
└── proposta-melhoria/
    └── proposta-melhoria.pdf    # Documento de melhoria de processo (4-6 páginas)
```

---

## Política de Atraso

- Até 1 dia: -20%
- Até 3 dias: -50%
- Após 3 dias: Não aceito

---

## Política de Integridade Acadêmica

### Avaliação Individual (Prova)

A prova é **estritamente individual**. Consulta permitida apenas à folha A4 manuscrita.

### Avaliações em Grupo (Projeto e Vídeo Final)

O projeto é desenvolvido em equipe. A contribuição individual é avaliada através de:
- Commits no repositório
- Contribuição demonstrada nos vídeos (todos devem aparecer no Vídeo Final)
- Capacidade de responder perguntas sobre qualquer parte do processo da equipe

### Uso de IA

O uso de ferramentas de IA (ChatGPT, Copilot, Claude etc.) é **permitido e até encorajado** para o desenvolvimento do projeto — afinal, um dos tópicos do curso é como integrar IA em processos de software. No entanto:

- Na **prova**, o uso de IA não é permitido
- Nos **vídeos de sprint e no Vídeo Final**, mencione quais ferramentas de IA a equipe usou e como
- Na **proposta de melhoria**, reflita sobre o impacto da IA no processo da equipe

### Consequências

- **1ª ocorrência**: Nota zero na atividade
- **2ª ocorrência**: Reprovação na disciplina
- **Casos graves**: Encaminhamento à coordenação

---

## Dúvidas Frequentes

**P: Posso usar o mesmo projeto em Processos e Web II?**  
R: Sim! Desde que os entregáveis sejam distintos. O Vídeo Final de Processos foca no **processo** (métricas, retrospectivas, VSM, evolução), enquanto o de Web II foca no **produto** (funcionalidades, código, gRPC/GraphQL).

**P: Por que substituiu a apresentação presencial pelo Vídeo Final?**  
R: Reorganização de cronograma após reposições. Vídeo dá mais flexibilidade para a equipe gravar com calma e permite janela maior para correção antes do fim do período.

**P: Todos os membros precisam aparecer no Vídeo Final?**  
R: A presença de todos os membros entra no critério "Comunicação" da avaliação do Vídeo Final.

**P: Cadê a Sprint 4?**  
R: Mesclada com a apresentação no Vídeo Final.

**P: Os Quizzes 6 e 7 foram cancelados?**  
R: Sim, na reorganização de 25/05. Permanecem os Quizzes 1, 2, 3 e 4.

**P: Preciso saber programar para este curso?**  
R: Sim, a equipe precisa desenvolver software. Mas a avaliação enfatiza o processo, não a complexidade técnica do código.


---

## Dúvidas e Suporte

### Canais de Atendimento

| Canal | Uso | Resposta |
|-------|-----|----------|
| Discord | Dúvidas, discussões | Até 24h |
| Aula presencial | Dúvidas conceituais | Imediato |
| Acompanhamento online | Revisão de projeto | Agendado |

### Horários de Atendimento

- **Presencial**: Após as aulas (12:00-12:30)
- **Online**: Discord, resposta até 24h em dias úteis
- **Acompanhamentos**: ver cronograma.