---
marp: true
theme: default
paginate: true
backgroundColor: #ffffff
color: #1a1a2e
style: |
  section {
    font-family: 'Calibri', sans-serif;
    padding: 36px 48px;
    font-size: 1.3em;
  }
  h1 {
    font-family: 'Consolas', monospace;
    color: #1a56db;
    font-size: 1.6em;
    margin-bottom: 0.3em;
    border-bottom: 2px solid #e5e7eb;
    padding-bottom: 0.2em;
  }
  h2 {
    font-family: 'Consolas', monospace;
    color: #374151;
    font-size: 1.2em;
    margin-bottom: 0.25em;
  }
  h3 { color: #6b7280; font-size: 0.9em; margin: 0.2em 0; }
  strong { color: #b45309; }
  em { color: #6b7280; }
  code {
    font-family: 'Consolas', monospace;
    background: #e5e7eb;
    color: #1e3a5f;
    padding: 0.08em 0.3em;
    border-radius: 3px;
    font-size: 1.00em;
  }
  pre {
    background: #f3f4f6 !important;
    border: 1px solid #d1d5db;
    border-left: 3px solid #1a56db;
    border-radius: 6px;
    padding: 0.7em 1em;
    margin: 0.4em 0;
  }
  pre code {
    background: transparent;
    color: #1e3a5f;
    font-size: 0.85em;
    padding: 0;
    line-height: 1.5;
  }
  table { font-size: 0.95em; width: 100%; border-collapse: collapse; }
  th {
    background: #e5e7eb;
    color: #1a56db;
    font-family: 'Consolas', monospace;
    padding: 0.35em 0.7em;
    border: 1px solid #d1d5db;
  }
  td { background: #ffffff; padding: 0.28em 0.7em; border: 1px solid #d1d5db; color: #1a1a2e; }
  tr:nth-child(even) td { background: #f9fafb; }
  ul { margin: 0.25em 0; padding-left: 1.3em; }
  li { margin: 0.18em 0; font-size: 0.88em; line-height: 1.4; }
  blockquote {
    border-left: 3px solid #1a56db;
    background: #eff6ff;
    padding: 0.4em 0.9em;
    margin: 0.5em 0;
    font-style: normal;
    color: #1e3a5f;
    border-radius: 0 5px 5px 0;
    font-size: 1.00em;
  }
  .columns { display: flex; gap: 1.8em; }
  .col { flex: 1; }
  .pill-red   { display:inline-block; background:#fee2e2; border:1.5px solid #dc2626; color:#dc2626; font-family:'Consolas',monospace; font-weight:bold; font-size:0.85em; padding:0.12em 0.6em; border-radius:20px; }
  .pill-green { display:inline-block; background:#dcfce7; border:1.5px solid #16a34a; color:#16a34a; font-family:'Consolas',monospace; font-weight:bold; font-size:0.85em; padding:0.12em 0.6em; border-radius:20px; }
  .pill-blue  { display:inline-block; background:#dbeafe; border:1.5px solid #1a56db; color:#1a56db; font-family:'Consolas',monospace; font-weight:bold; font-size:0.85em; padding:0.12em 0.6em; border-radius:20px; }
  .tag { display:inline-block; background:#f3f4f6; border:1px solid #d1d5db; color:#374151; font-size:0.85em; padding:0.1em 0.5em; border-radius:4px; font-family:'Consolas',monospace; }

---

# VSM: Gargalos e Melhorias

## Do mapa do estado atual a um plano de ação

**Processos de Software — Sprint 3**

**Prof. Fernando** · UFRN · 2026.1

---

# De onde paramos

Aula passada: cada equipe desenhou o **VSM do estado atual** do projeto.

| Já temos | Hoje |
|---|---|
| Mapa do fluxo, com caixas e filas | Achar o **gargalo** com método |
| PT, LT e %C&A por etapa | Calcular o **impacto** de cada fila |
| Lead time total e eficiência de fluxo | Propor **melhorias mensuráveis** |

> Objetivo de hoje: sair com um VSM revisado, **um gargalo identificado com dados** e **1–2 melhorias** que cabem na entrega da Sprint 3.

---

# Revisão: as métricas que vamos usar

| Métrica | Lê-se |
|---|---|
| **PT** — process time | Quanto tempo de **trabalho** a etapa consome |
| **LT** — lead time | Quanto tempo o item **passa** na etapa (com fila) |
| **%C&A** | % de itens que saem da etapa **sem precisar voltar** |
| **Eficiência de fluxo** | Σ PT ÷ lead time total |

> Hoje a métrica-chave é a diferença `LT − PT`: é o **tempo de espera** de cada etapa. A etapa com a maior espera é a primeira suspeita de gargalo.

---

# O que é um gargalo

Gargalo é a etapa que **limita a vazão do fluxo inteiro**.

```
Capacidade:   Análise      Código       Review       Deploy
              20 itens/sem  15/sem    ▶ 5/sem ◀     30/sem

Vazão do sistema inteiro = 5 itens/semana  ← o gargalo MANDA
```

> Não importa quão rápidas são as outras etapas: o sistema **inteiro** entrega na velocidade do gargalo. Acelerar Análise de 20 para 40 não muda **nada** — Review continua liberando 5/semana.

---

# Como o gargalo aparece no VSM

Três sinais denunciam o gargalo no mapa:

| Sinal | No diagrama |
|---|---|
| Maior **fila** antes da etapa | Triângulo "gordo" — itens acumulados |
| Maior **espera** (`LT − PT`) | Escada com degrau longo de espera |
| Menor **%C&A** a montante | Retrabalho empurrando volume para trás |

```
┌────────┐   ▽▽▽▽▽   ┌────────┐   ▽   ┌────────┐
│ Código │ →  fila →  │ Review │ →  →  │ Deploy │
└────────┘   3 dias   └────────┘ 4h    └────────┘
                      ▲ aqui: maior fila, maior espera
```

> O gargalo quase nunca é "as pessoas são lentas". É estrutural: uma pessoa só revisa, CI demora, ambiente de teste é compartilhado, aprovação depende de alguém de fora.

---

# Teoria das Restrições em uma frase

Goldratt (*A Meta*): **todo sistema tem uma restrição; melhorar qualquer coisa que não seja a restrição é ilusão de progresso.**

Os cinco passos de foco:

1. **Identificar** a restrição (o gargalo)
2. **Explorar** — tirar o máximo dela sem investir (ex.: tirar trabalho não essencial da fila)
3. **Subordinar** — alinhar o resto do fluxo ao ritmo dela
4. **Elevar** — aí sim, investir para aumentar a capacidade
5. **Repetir** — quebrado um gargalo, outro surge

> O passo 2 vem antes do 4 de propósito: muita melhoria sai **de graça**, só reorganizando. Investir (passo 4) é o último recurso, não o primeiro.

---

# Da fila ao gargalo: quantifique

Não basta dizer "review é lento". Mostre com número:

```
Etapa Review do projeto:
  LT = 3 dias 1h     PT = 1h     espera = 3 dias
  → 73% do lead time total do projeto está NESTA fila
```

| Pergunta do workshop | Resposta esperada |
|---|---|
| Qual etapa tem a maior espera? | _____ (em horas/dias) |
| Que % do LT total ela representa? | _____ % |
| Quantos itens ficam parados nela em média? | _____ |
| O que faz a fila crescer? | _____ |

> A entrega da Sprint 3 pede gargalos **com dados**. "Achamos que é o review" não conta. "O review concentra 73% do lead time, com 4 PRs parados em média" — isso conta.

---

# Por que a fila existe? Os 5 porquês

Achado o gargalo, encontre a **causa raiz** — não pare no primeiro sintoma:

```
Problema: PRs ficam 3 dias esperando review.
  Por quê? → Só o líder técnico revisa.
  Por quê? → Ninguém mais se sente seguro para aprovar.
  Por quê? → Não há critério claro do que checar num review.
  Por quê? → Nunca foi combinado em equipe.
  Por quê? → A equipe nunca discutiu seu próprio processo de review.
                                  ↑ causa raiz — e é acionável
```

> O primeiro "porquê" leva a uma solução fraca ("cobrar o líder"). O quinto leva a uma solução real ("definir um checklist de review e habilitar mais revisores"). Cave fundo.

---

# De causa raiz a melhoria mensurável

Uma boa melhoria tem **três partes**: ação, métrica e meta.

| Parte | Exemplo ruim | Exemplo bom |
|---|---|---|
| Ação | "melhorar o review" | "criar checklist de review + 2 revisores aptos" |
| Métrica | (nenhuma) | espera média na fila de review |
| Meta | "ficar mais rápido" | "de 3 dias para < 1 dia até a Sprint 4" |

> Sem métrica e meta, não dá para saber na Sprint 4 se a melhoria funcionou. "Melhorar" não é verificável; "reduzir a espera de review de 3 dias para menos de 1" é.

---

# Explorar

Muita melhoria de fluxo **não custa nada** — só combinação de equipe:

| Gargalo comum | Melhoria de baixo custo (passo "explorar") |
|---|---|
| Fila de review longa | Checklist de review + WIP limit de PRs abertos |
| PRs gigantes, difíceis de revisar | Limitar tamanho de PR — quebrar em partes menores |
| CI lento | Cache de dependências (visto na Sprint 2!) |
| Retrabalho alto | "Definition of Done" clara antes de abrir o PR |
| Item parado no backlog | Refinar e priorizar na daily |

> Repare: várias dessas saíram de conteúdos que vocês **já viram** — WIP limits (Kanban, Sprint 1), cache no CI (Sprint 2). A Sprint 3 conecta tudo.

---

# Atividade - Refine o VSM do projeto

Em equipe, agora. Cinco passos:

1. **Revisem** o VSM da aula passada — está honesto? Falta alguma fila?
2. **Calculem** a espera (`LT − PT`) de cada etapa e ordenem.
3. **Identifiquem o gargalo** — a etapa com maior espera. Quantifiquem (% do LT total).
4. **5 porquês** sobre o gargalo — até chegar a uma causa raiz acionável.
5. **Escrevam 1–2 melhorias** no formato ação + métrica + meta.

> No fim, cada equipe deve ter: VSM revisado, **um gargalo quantificado** e **melhorias mensuráveis**. Isso é o esqueleto do vídeo da Sprint 3.

---

# Modelo de registro da equipe

Anotem assim — vai direto para o vídeo e para a Sprint 4:

```
GARGALO IDENTIFICADO
  Etapa: ..............................
  Espera média: .......  (% do lead time total: ......%)
  Itens parados em média: ......

CAUSA RAIZ (5 porquês): ..............................

MELHORIA 1
  Ação: ................................................
  Métrica: ............  Atual: ........  Meta: ........
```

> Guardem os **números de hoje**. Na Sprint 4 vocês vão comparar: o lead time caiu? A melhoria funcionou? Sem o "antes", não há o que comparar.

---

# Erros comuns

| Erro | Consequência |
|---|---|
| Apontar um gargalo "no chute" | Otimiza o lugar errado — TOC ignorada |
| Parar no 1º porquê | Solução superficial, gargalo volta |
| Melhoria sem métrica/meta | Impossível avaliar na Sprint 4 |
| Querer consertar 5 gargalos de uma vez | TOC: foque na **restrição atual** |
| Pular o "explorar", ir direto para "investir" | Gasta esforço onde uma combinação resolveria |
| VSM maquiado para parecer bom | Esconde o problema que o exercício quer achar |

> Foco em **um** gargalo. Resolvido ele, o próximo aparece — e aí o ciclo recomeça (passo 5 da TOC). Querer tudo de uma vez não resolve nada.

---

# Checklist antes de ir embora

Alimenta a Sprint 3 <span class="tag">prazo sprint: 29/05</span>:

- [ ] VSM do estado atual revisado e honesto
- [ ] Espera (`LT − PT`) calculada por etapa
- [ ] Gargalo identificado **e quantificado** (% do LT total)
- [ ] Causa raiz encontrada via 5 porquês
- [ ] 1–2 melhorias no formato ação + métrica + meta
- [ ] Números do "estado atual" registrados para comparar na Sprint 4

> Com gargalo quantificado e melhorias mensuráveis registradas, a parte de análise da Sprint 3 está pronta. Falta gravar o vídeo.

---

# Próximos passos

- **26/05 (ter)** — Controle de qualidade de processos: como o **code review** estruturado e as **inspeções** atacam justamente o gargalo mais comum que vocês acharam hoje.
- **28/05 (qui)** — Acompanhamento online: Sprint 3 + revisão para a prova.
- **Sprint 3** (prazo **29/05**) — vídeo 8 min: VSM do estado atual, gargalos com dados, melhorias propostas, evolução das métricas DORA entre as Sprints 2 e 3.
- **02/06 (ter)** — Prova escrita das Unidades 1 e 2.

> A melhoria que vocês desenharam hoje vira a base do **VSM do estado futuro** — entregável da Sprint 4.

---

# Referências da aula

- Goldratt — *A Meta* — Teoria das Restrições e os cinco passos de foco
- Martin & Osterling — *Value Stream Mapping* (cap. 1) — leitura **L12**
- Reinertsen — *The Principles of Product Development Flow* — economia de filas
- Kim et al. — *The DevOps Handbook* — o Primeiro Caminho (fluxo)
- DORA — *Four Keys* — [dora.dev/guides/dora-metrics-four-keys](https://dora.dev/guides/dora-metrics-four-keys/)
