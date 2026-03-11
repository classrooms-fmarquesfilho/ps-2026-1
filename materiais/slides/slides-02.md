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
    font-size: 0.9em;
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

# Modelos de Ciclo de Vida
## Cascata, Espiral, Modelo V e a Transição para o Ágil

**Prof. Fernando** · DIMAp/UFRN · 2026.1

*De Royce (1970) a Boehm (1988) — e por que mudamos*

---

# O artigo mais mal interpretado da história

## Royce, 1970 — "Managing the Development of Large Software Systems"

> Royce **nunca** usou a palavra "waterfall" (cascata).

O diagrama sequencial que todo mundo conhece aparece na **página 2** do artigo. Mas Royce imediatamente diz:

> *"I believe in this concept, but the implementation described above is risky and invites failure."*

O resto do artigo propõe **iterações, protótipos e feedback** entre fases.

### O que aconteceu:
- O DoD (Departamento de Defesa dos EUA) adotou o diagrama da página 2
- Ignorou as 9 páginas seguintes de ressalvas
- Virou o padrão MIL-STD-2167 (1985)

---

# A Cascata como ela é

## Modelo sequencial — cada fase termina antes da próxima começar

```
  Requisitos ──→ Projeto ──→ Implementação ──→ Testes ──→ Implantação
       │                                                      │
       └──────── sem retorno fácil entre fases ───────────────┘
```

### Premissas (raramente verdadeiras):
- Requisitos são conhecidos e estáveis desde o início
- Erros são encontrados na fase em que ocorrem
- O cliente sabe exatamente o que quer

### Onde ainda faz sentido:
- Sistemas embarcados críticos (aviação, medicina)
- Contratos governamentais com requisitos fixos
- Quando o custo de falha é catastrófico e os requisitos são estáveis

---

# Modelo V — teste como espelho

## Cada fase de desenvolvimento tem uma fase de teste correspondente

```
  Requisitos  ──────────────────────────  Testes de Aceitação
       │                                         │
    Projeto de Sistema  ──────────  Testes de Sistema
          │                                │
       Projeto Detalhado  ────  Testes de Integração
             │                        │
          Implementação ── Testes Unitários
```

### A ideia central:
- Planejar os testes **ao mesmo tempo** que se define cada nível
- Rastreabilidade: cada requisito tem um teste correspondente

### Limitação:
Herda o problema da cascata — assume requisitos estáveis.
Mas a ênfase em testes em cada nível é uma contribuição duradoura.

---

# A Espiral de Boehm (1988)

## Modelo orientado a risco — cada ciclo avalia o que pode dar errado

```
         ┌── Determinar objetivos ──┐
         │                          │
    Planejar ◄──── ESPIRAL ────► Identificar riscos
    próxima volta  (iteração)       │
         │                     Desenvolver + verificar
         └──────────────────────────┘
```

### As 4 atividades de cada volta:
1. **Definir objetivos** — o que queremos desta iteração?
2. **Analisar riscos** — o que pode dar errado? Prototipar.
3. **Desenvolver e verificar** — construir o incremento
4. **Planejar** a próxima volta

### Contribuição fundamental:
**Risco como critério de decisão.** Antes de codificar, pergunte: "qual é o maior risco?"

---

# Iterativo e Incremental

## A base conceitual dos métodos ágeis

```
  Iteração 1:  [Requisitos → Design → Código → Teste] → Incremento 1
  Iteração 2:  [Requisitos → Design → Código → Teste] → Incremento 2
  Iteração 3:  [Requisitos → Design → Código → Teste] → Incremento 3
                                                            ↓
                                                     Produto cresce
                                                     a cada ciclo
```

### Dois conceitos distintos:
- **Iterativo**: refinar o mesmo artefato em ciclos sucessivos
- **Incremental**: adicionar funcionalidade a cada ciclo

### Vantagem crucial:
Feedback do cliente a cada incremento — não só no final.
Erros são descobertos cedo, quando são baratos de corrigir.

---

# RUP — Rational Unified Process

## Tentativa de unificar cascata e iteração

```
        Concepção │ Elaboração │ Construção │ Transição
  ─────────┬──────┼────────────┼────────────┼───────────
  Requisitos  ████│████████    │  ██        │
  Análise     ██  │██████████  │  ████      │
  Projeto         │  ████████  │████████    │  ██
  Implementação   │    ████    │██████████  │████
  Teste           │      ██   │  ████████  │████████
```

### Características:
- 4 fases, cada uma com múltiplas iterações
- Atividades ocorrem em paralelo (com intensidades diferentes)
- Pesado em documentação e artefatos UML

### Por que importa:
RUP foi a ponte entre o mundo sequencial e o ágil. Introduziu iterações em contextos corporativos conservadores.

---

# A transição para o Ágil

## Por que o mundo migrou?

| Problema do modelo tradicional | Solução ágil |
|-------------------------------|--------------|
| Requisitos mudam (e sempre vão mudar) | Abraçar mudança, ciclos curtos |
| Feedback só no final | Demo a cada sprint |
| Planejamento extenso desperdiçado | Planejar "just enough" |
| Documentação que ninguém lê | Software funcionando > documentação |
| Equipes desconectadas do cliente | Colaboração contínua |

### 2001 — Manifesto Ágil
17 desenvolvedores se reuniram em Snowbird, Utah, e escreveram:

> *Indivíduos e interações* mais que processos e ferramentas
> *Software funcionando* mais que documentação abrangente
> *Colaboração com o cliente* mais que negociação de contratos
> *Responder a mudanças* mais que seguir um plano

---

# Comparativo: quando usar o quê?

| Modelo | Quando faz sentido | Quando NÃO usar |
|--------|--------------------|-----------------|
| **Cascata** | Requisitos fixos, regulação pesada | Projetos com incerteza |
| **Modelo V** | Sistemas críticos, testes rigorosos | Quando requisitos evoluem |
| **Espiral** | Alto risco, necessidade de protótipos | Projetos pequenos/simples |
| **Iterativo** | Maioria dos projetos modernos | Contratos rígidos de escopo fixo |
| **Ágil (Scrum, XP)** | Incerteza, feedback rápido | Domínios regulados sem adaptação |

### Na prática (2026):
- ~70% do mercado usa alguma variação de ágil
- Domínios regulados (saúde, aviação, financeiro) usam **híbridos**
- O importante é entender os **trade-offs**, não defender um modelo

---

# Linha do tempo

## De 1970 a 2026 — 56 anos de evolução

```
  1970  Royce — Cascata (mal interpretado)
  1981  Modelo V — ênfase em verificação
  1986  Takeuchi & Nonaka — "Scrum" (artigo original na HBR)
  1988  Boehm — Espiral (orientado a risco)
  1996  RUP — Iterativo em contexto corporativo
  1999  Beck — Extreme Programming
  2001  Manifesto Ágil — ruptura filosófica
  2004  Schwaber — Scrum Guide (1ª edição)
  2009  Flickr — "10+ deploys per day" (DevOps)
  2013  Kim et al. — The Phoenix Project (DevOps como cultura)
  2018  Forsgren et al. — Accelerate (DORA)
  2024  DORA — AI Productivity Paradox
  2026  Vocês — aprendendo a escolher o processo certo 😄
```

---

# Resumo

## O que vimos hoje:

- **Cascata** (Royce, 1970) — sequencial, mas o autor sabia das limitações
- **Modelo V** — teste como espelho do desenvolvimento
- **Espiral** (Boehm, 1988) — risco como critério de decisão
- **Iterativo/Incremental** — base conceitual do ágil
- **RUP** — ponte entre o mundo corporativo e as iterações
- **Manifesto Ágil** (2001) — a ruptura filosófica

### Aguardem o Vídeo 1: **Scrum**

**Leiam o Guia do Scrum 2020 (13 págs) e o Manifesto Ágil!**

Até a próxima! 🎓