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

# IA em Processos de Software

## E o fechamento: maturidade e melhoria contínua

**Processos de Software — Unidade 3 (conteúdo final, parte 2/2)**

**Prof. Fernando** · UFRN · 2026.1

---

# De onde viemos

O curso foi montando uma caixa de ferramentas:

| Vimos | Para |
|---|---|
| Scrum, XP, Lean, Kanban | organizar o trabalho |
| DevOps, CI/CD, Docker | automatizar a entrega |
| DORA, VSM | medir e enxergar o fluxo |
| Team Topologies | organizar as equipes |

> Falta uma força que hoje atravessa tudo isso: a **IA**. Como ela muda processos — para melhor e para pior.

---

# O Paradoxo da Produtividade

A IA escreve código mais rápido. Logo, o time entrega mais valor... **será?**

```
Mais código gerado   ≠   mais valor entregue
Mais commits         ≠   produto melhor
"Senti que rendi"    ≠   o sistema melhorou
```

> O paradoxo: ganho **percebido** de produtividade individual nem sempre vira ganho de **entrega** da equipe. Atividade não é resultado.

---

# O que os dados sugerem

Relatórios DORA (2024–2025) sobre adoção de IA:

| Observação | Leitura |
|---|---|
| Adoção de IA cresce rápido | quase todo time já usa de alguma forma |
| Ganhos de fluxo **não** são automáticos | dependem das boas práticas em volta |
| Sem práticas sólidas, a **estabilidade** pode piorar | mais mudanças, mais risco, mais retrabalho |

> A IA **amplifica** o processo que já existe: processo bom melhora; processo frágil piora mais rápido. (detalhes na leitura **L18**)

---

# Medir o impacto da IA

A armadilha é medir **atividade**. Meça **resultado** — com o que já sabem:

| Não meça (atividade) | Meça (resultado) |
|---|---|
| Linhas de código geradas | Lead time para mudanças (DORA) |
| Nº de sugestões aceitas | Taxa de falha em mudanças (DORA) |
| "Quanto a IA ajudou?" (opinião) | Frequência de deploy, tempo de recuperação |

> Querem saber se a IA ajudou o processo? Olhem as **métricas DORA antes e depois** — exatamente o que a Proposta de Melhoria pede.

---

# DORA AI Capabilities Model

A DORA identificou **capacidades organizacionais** que fazem a IA gerar valor (em vez de ruído). Entre elas:

- Política clara e comunicada sobre **uso de IA**
- **Dados internos** saudáveis e acessíveis
- Trabalhar em **lotes pequenos** (small batches)
- **Plataforma interna** de qualidade
- Foco **centrado no usuário**
- Boas práticas de **controle de versão** e revisão

> Quase tudo já é tema do curso. A IA não substitui processo bom — ela **exige** processo bom. (ver leitura **L18**)

---

# Governança de IA em processos

Usar IA com responsabilidade exige combinados explícitos:

| Tema | Pergunta que a equipe deve responder |
|---|---|
| **Transparência** | Declaramos onde a IA foi usada? |
| **Revisão** | Código gerado por IA passa por review como qualquer outro? |
| **Dados** | Que dados podem (e não podem) ir para a ferramenta? |
| **Responsabilidade** | Quem responde pelo código? A pessoa, sempre |
| **Supervisão** | Há um humano no circuito nas decisões que importam? |

> Governança não é proibir IA — é usá-la sem abrir mão de qualidade, segurança e responsabilidade.

---

# IA no projeto de vocês

A Entrega Final pede isto de forma explícita:

- **Declarem** no vídeo e na Proposta **quais** ferramentas de IA usaram e **como**
- **Reflitam**: a IA mudou seu lead time? Seu retrabalho? Sua revisão?
- Conectem ao **Paradoxo**: mediram valor entregue, ou só sentiram que renderam?

> É preciso avaliar criticamente qualquer ferramenta que vocês usam com frequência.

---

# Fechando: maturidade de processos

Como uma organização **institucionaliza** boas práticas e melhora ao longo do tempo?

| Modelo | Ideia central |
|---|---|
| **CMMI V3.0** | Níveis de maturidade/capacidade — do caótico ao "em otimização contínua" |
| **ISO/IEC 12207** | Padrão dos **processos do ciclo de vida** de software |

> Cuidado com a leitura errada: maturidade **não** é burocracia. É a capacidade de executar e **melhorar** o processo de forma consistente.

---

# Maturidade ≠ burocracia

O nível mais alto de maturidade é, justamente, **melhoria contínua**:

```
Caótico → Repetível → Definido → Medido → Em otimização contínua
                                              ↑ Kaizen, retrospectivas, métricas
```

> Ágil, Lean e DevOps bem-feitos **são** processos maduros: vocês medem (DORA), enxergam (VSM), refletem (retro) e melhoram. Maturidade moderna = capacidade de melhorar.

---

# A jornada do curso

1. **Processo é produto** — a qualidade do processo importa tanto quanto o software
2. **Meça** — DORA, fluxo; decisão por dado, não por opinião
3. **Enxergue o fluxo** — o VSM revela onde o tempo é perdido
4. **Organize times** — Conway, Team Topologies; estrutura molda fluxo
5. **Melhore sempre** — retrospectivas, causa raiz, Kaizen

> A Proposta de Melhoria de vocês é a síntese do curso em um documento: medir, enxergar, analisar, propor.

---

# Para levar para a profissão

- O melhor processo é o que a equipe **realmente segue** e **melhora**
- Métricas servem para **aprender**, não para punir
- Desconfie de soluções "mágicas" (inclusive IA) sem medir resultado
- Lotes pequenos, feedback rápido e fluxo valem em **qualquer** stack

> É importante dominar o vocabulário, conceitos, técnicas, ferramentas e práticas para diagnosticar e melhorar qualquer processo de entrega de software.

---

# Entrega Final — 29/06 (seg)

Tudo isto alimenta a entrega que encerra o curso:

- **Vídeo (12 min)**: MVP + foco no **processo** (evolução, Kanban, VSM, DORA)
- **Proposta de Melhoria (PDF)**: VSM, análise de problemas, ações com métricas-alvo
- **Reflexão** sobre IA e sobre a organização do trabalho

> Prazo: **29/06 (seg), 23:59**. 

---

# Referências da aula

- DORA (2025) — *AI Capabilities Model* — leitura **L18**
- DORA — *State of DevOps* (capítulos sobre IA) — [dora.dev](https://dora.dev/)
- CMMI Institute — *CMMI V3.0* — modelo de maturidade
- ISO/IEC 12207 — processos do ciclo de vida de software
- Skelton & Pais — *Team Topologies* (revisão)
