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

# Value Stream Mapping

## Enxergar o fluxo inteiro — da ideia ao deploy

**Processos de Software — Sprint 3 (teoria + atividade)**

**Prof. Fernando** · UFRN · 2026.1

---

# De onde paramos

Sprint 2: o time aprendeu a **automatizar** (pipeline, Docker) e a **medir** (métricas DORA).

| Já temos | Hoje |
|---|---|
| Pipeline rodando | Olhar o **fluxo inteiro**, não só o CI |
| Dois números DORA | Entender **de onde** vêm esses números |
| "A entrega está mais rápida" | **Onde** exatamente o tempo é gasto — e perdido |

> A Sprint 3 é a mais **reflexiva** do semestre: sai do "fazer" e entra no "analisar". Hoje começa pela ferramenta central — o VSM.

---

# Plano da aula

1. O que é um Value Stream — e por que mapear <span class="tag">~10 min</span>
2. Anatomia de um VSM: processos, filas, métricas <span class="tag">~15 min</span>
3. Lead time vs cycle time vs %C&A <span class="tag">~10 min</span>
4. **Atividade**: mapear o estado atual do seu projeto <span class="tag">~25 min</span>

---

# O que é um Value Stream

Um **fluxo de valor** é toda a sequência de passos para transformar uma **ideia** em **valor entregue** ao usuário.

```
IDEIA → backlog → análise → código → review → teste → deploy → USUÁRIO
```

> A pergunta do VSM não é "esse passo é rápido?". É: **"da ideia ao usuário, quanto tempo passa — e quanto desse tempo foi realmente trabalho?"**

VSM vem do Lean da Toyota (lembram da Sprint 1: *muda*, *mura*, *muri*). Aqui aplicamos a mesma lente ao processo de software.

---

# Por que mapear o fluxo todo

A intuição engana. Times "sentem" onde está o problema — e erram.

```
Percepção do time:  "código é a parte lenta — somos poucos devs"
Realidade do VSM:   código leva 4h; mas o PR fica 3 DIAS esperando review
```

| Sem VSM | Com VSM |
|---|---|
| Otimiza o que é **visível** (escrever código) | Otimiza o que é **lento** (a fila do review) |
| Decisão por opinião | Decisão por **dado** |
| Melhoria local, ganho global zero | Ataca o gargalo de verdade |

> Otimizar um passo que não é o gargalo **não acelera nada**. O VSM existe para você não gastar esforço no lugar errado.

---

# Trabalho vs espera

A revelação central do VSM: a maior parte do lead time costuma ser **espera**, não trabalho.

```
| análise |  ESPERA   | código |   ESPERA    | review | ESPERA | deploy |
   2h        1 dia       4h        3 dias        1h      4h        20min
└──────────────── trabalho: ~7h ────────────────────────────────────┘
└──────────────── lead time total: ~4,7 dias ───────────────────────┘
```

| Tipo de tempo | No exemplo | É... |
|---|---|---|
| Trabalho (agrega valor) | ~7h | o que o cliente "pagaria" |
| Espera / fila (não agrega) | ~4 dias | *muda* — desperdício puro |

> Se ~85% do tempo é fila, contratar mais devs (acelerar as ~7h de trabalho) quase não move o lead time. **Atacar as filas, sim.**

---

# Anatomia de um VSM

Três elementos no diagrama:

| Elemento | Símbolo | O que representa |
|---|---|---|
| **Caixa de processo** | retângulo | Um passo onde há trabalho (análise, código, review) |
| **Fila / espera** | triângulo | Item parado esperando o próximo passo |
| **Linha do tempo** | escada embaixo | Alterna tempo de trabalho e tempo de espera |

```
┌────────┐  ▽  ┌────────┐  ▽  ┌────────┐
│ Código │ →   │ Review │ →   │ Deploy │
└────────┘     └────────┘     └────────┘
  4h    3 dias   1h    4h      20min
```

> Cada caixa carrega suas métricas. O triângulo entre as caixas é onde a maioria das equipes descobre que está perdendo seu lead time.

---

# As três métricas de cada caixa

| Métrica | Sigla | O que mede |
|---|---|---|
| **Lead Time** | LT | Tempo total: entrou na etapa → saiu (inclui espera) |
| **Process Time** | PT | Tempo de trabalho efetivo na etapa |
| **% Completo e Acurado** | %C&A | % de itens que chegam sem precisar retrabalho |

```
Etapa "Review":  LT = 3 dias 1h  |  PT = 1h  |  %C&A = 70%
```

> %C&A é a métrica que o pessoal esquece. Se a etapa de review recebe 30% dos PRs com problema (código que nem compila, sem teste), esse retrabalho **volta** para etapas anteriores — e infla o lead time de todo mundo.

---

# Lead time vs cycle time

Dois termos que aparecem juntos e se confundem — voltam da Sprint 1 (Kanban):

| Termo | Mede | Relógio |
|---|---|---|
| **Lead time** | Pedido feito → entregue | Começa quando o **cliente** pede |
| **Cycle time** | Trabalho começou → terminou | Começa quando a **equipe** pega |

```
| ITEM NO BACKLOG (espera) | equipe pega → ... → entrega |
└──────────────── lead time ────────────────────────────┘
                            └──── cycle time ────────────┘
```

> A diferença entre os dois é **tempo na fila do backlog**. Cliente sente o lead time. Se o cycle time é bom mas o lead time é péssimo, o gargalo está **antes** do trabalho começar — na priorização.

---

# A eficiência do fluxo

Uma razão simples resume a saúde do fluxo:

```
                    tempo de trabalho (Σ PT)
Eficiência de fluxo = ───────────────────────────
                    lead time total
```

```
Exemplo:   7h de trabalho / 4,7 dias de lead time ≈ 7 / 56  ≈  12%
```

| Eficiência típica | Leitura |
|---|---|
| 5–15% | Comum — muito tempo em fila |
| 25–40% | Fluxo bem cuidado |
| > 40% | Raro — fluxo muito enxuto |

> Não se assuste com 12%. É **normal**. O valor do número não é a nota — é o **ponto de partida**: agora você sabe que há ~88% de tempo de fila para investigar.

---

# VSM e DORA: como se conectam

Não são ferramentas concorrentes — uma alimenta a outra:

| DORA | VSM |
|---|---|
| **Mede** o resultado (lead time, frequência) | **Explica** o resultado (onde o tempo vai) |
| "Lead time = 4,7 dias" | "...porque review fica 3 dias na fila" |
| Diz **que** há um problema | Diz **onde** está o problema |

> Na Sprint 2 vocês coletaram o **número**. O VSM da Sprint 3 abre esse número e mostra **a anatomia** dele. Juntos: DORA aponta o sintoma, VSM localiza a causa.

---

# Estado atual vs estado futuro

O VSM se usa em duas versões:

| Estado atual | Estado futuro |
|---|---|
| O fluxo **como ele é hoje** | O fluxo **como deveria ser** |
| Honesto, sem maquiar | Realista, com melhorias concretas |
| Entregável de **hoje** (Sprint 3) | Entregável da **Sprint 4** |

> Hoje e no workshop de 21/05 vocês desenham o **estado atual**. A regra é uma só: **sem maquiar**. Um VSM bonito e falso não serve para nada — o objetivo é enxergar o problema, não escondê-lo.

---

# Atividade: mapear o estado atual

Em equipe, agora — desenhem o VSM do **seu projeto** (papel, quadro ou Miro):

1. Listem as **etapas** do fluxo: ideia → backlog → código → review → CI → deploy.
2. Para cada etapa, estimem **PT** (trabalho) e **LT** (com espera).
3. Marquem as **filas** (triângulos) entre as etapas.
4. Calculem o **lead time total** e a **eficiência de fluxo**.
5. Anotem: onde está a **maior fila**?

> Usem dados **reais** do projeto — histórico de PRs no GitHub, datas de commit e merge (igual à coleta DORA da Sprint 2). Estimativa honesta vale mais que precisão inventada.

---

# Onde buscar os dados reais

Vocês já coletaram material parecido na Sprint 2. Reaproveitem:

```bash
# tempo entre primeiro commit de uma branch e o merge na main
git log --pretty="%h %ci %s" main

# PRs e suas datas (data de abertura → data de merge = fila do review)
# → aba "Pull requests" → filtro "is:merged"
```

| Etapa do VSM | Onde achar o tempo |
|---|---|
| Backlog → início | Data do card no GitHub Projects → 1º commit |
| Código | 1º commit → PR aberto |
| Review (fila!) | PR aberto → PR aprovado |
| CI | Duração do workflow na aba Actions |
| Deploy | Merge → publicação |

> Não precisa de precisão de cronômetro. Ordem de grandeza ("horas" vs "dias") já revela o gargalo.

---

# Erros comuns ao montar o VSM

| Erro | Por que atrapalha |
|---|---|
| Mapear o fluxo "ideal" em vez do real | Esconde justamente o que você quer achar |
| Esquecer as filas (só caixas de processo) | A fila é onde mora o desperdício |
| Misturar PT e LT | Perde a distinção trabalho vs espera |
| Mapear granular demais (15 etapas) | Vira diagrama, não vira análise |
| Ignorar %C&A | Não enxerga o retrabalho escondido |
| Fazer sozinho, sem o time | Cada um conhece um pedaço do fluxo |

> Comece grosso: 5–7 etapas. Dá para refinar depois. Um VSM com 15 caixas costuma ser bonito e inútil.

---

# Checklist antes de ir embora

Atividade VSM — base para a Sprint 3 <span class="tag">prazo sprint: 29/05</span>:

- [ ] Etapas do fluxo do projeto listadas (5–7 caixas)
- [ ] Filas marcadas entre as etapas
- [ ] PT e LT estimados por etapa, com dados reais
- [ ] Lead time total e eficiência de fluxo calculados
- [ ] Maior fila identificada — candidata a gargalo

> Se a equipe sai daqui com um rascunho honesto do estado atual e sabe **qual é a maior fila**, a aula cumpriu o objetivo.

---

# Próximos passos

- **21/05 (qui)** — VSM (continuação): refinar o mapa, **quantificar gargalos** e propor 1–2 melhorias mensuráveis.
- **26/05 (ter)** — Controle de qualidade de processos: code review estruturado, inspeções Fagan, métricas de processo.
- **Sprint 3** (prazo 29/05) — vídeo 8 min com o VSM do estado atual e a análise de gargalos.
- **Pergunta para levar**: "Se a equipe pudesse eliminar **uma única fila** do mapa, qual daria o maior ganho de lead time — e por quê?"

> Acompanhamento online: **28/05 (qui)** — Sprint 3 + revisão para a prova de 02/06.

---

# Referências da aula

- Martin & Osterling — *Value Stream Mapping* (cap. 1) — leitura **L12**
- Rother & Shook — *Learning to See* — a obra clássica de VSM
- DORA — *Four Keys* — [dora.dev/guides/dora-metrics-four-keys](https://dora.dev/guides/dora-metrics-four-keys/)
- Kim et al. — *The DevOps Handbook* — fluxo de valor e o Primeiro Caminho
- Reinertsen — *The Principles of Product Development Flow* — teoria de filas
