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

# Processos de Software
## Apresentação do Curso

**Prof. Fernando** · DIMAp/UFRN · 2026.1

*Por que processos importam — especialmente na era da IA*

---

# O que é um processo de software?

> Um **processo de software** é um conjunto de atividades, métodos e práticas usados para desenvolver e manter software.

- Quem faz o quê, quando, e como
- Como a equipe se organiza e se comunica
- Como o trabalho flui do "a gente precisa disso" até "tá em produção"

### O que NÃO é processo:
- Não é burocracia
- Não é documentação por documentação
- Não é o oposto de agilidade

---

# Por que estudar processos?

## O software está em tudo — e fica cada vez mais complexo

- Equipes distribuídas (pós-pandemia permaneceu)
- Ciclos de entrega cada vez menores (deploy contínuo)
- **IA gerando código** em escala industrial

### O desafio mudou:

```
  Antigamente:  "Como escrever código?"
  Hoje:         "Como organizar pessoas, ferramentas e práticas
                 para entregar software que funciona?"
```

**Processo é o que diferencia uma equipe que entrega de uma que sofre.**

---

# O caso XZ Utils — CVE-2024-3094

## Engenharia social de 3 anos contra o open source

```
2021  "Jia Tan" começa a contribuir com patches legítimos
2022  Contas falsas (Jigar Kumar, krygorin4545) pressionam
      o mantenedor original — "o projeto está lento"
2023  Jia Tan vira co-mantenedor oficial do XZ Utils
2024  Backdoor inserido nas versões 5.6.0 e 5.6.1
      → Execução remota de código via SSH
      → CVSS 10.0 (nota máxima de severidade)
```

**Descoberto por acaso**: Andres Freund (Microsoft/PostgreSQL) notou SSH 500ms mais lento que o normal.

---

# XZ Utils — O que o processo tem a ver?

## Falhas de processo que permitiram o ataque:

- **Mantenedor solo** sobrecarregado e sem suporte
- **Revisão de código** insuficiente (1 pessoa = 0 revisão)
- **Confiança sem verificação** — commit access concedido por conveniência
- **Tarballs diferentes do Git** — o código malicioso só existia no pacote de distribuição

### O que teria impedido:

- Processo de revisão obrigatória (2+ revisores)
- Builds reproduzíveis (tarball = git)
- Rotação e auditoria de mantenedores
- Diversidade de contribuidores

**→ Processo salva projetos. Processo salva infraestrutura crítica.**

---

# IA e código: o paradoxo da produtividade

## Os números impressionam — mas não contam toda a história

| Métrica | Dado |
|---------|------|
| Adoção de IA por devs | ~90% usam alguma ferramenta (DORA 2024) |
| Commits via Claude Code | 4% de todos os commits públicos no GitHub |
| Microsoft → Anthropic | ~US$ 500 milhões/ano em modelos Claude |
| Receita Anthropic | US$ 14 bilhões (run-rate 2026) |

### Relato real:
*"Meu amigo na Microsoft gasta US$ 400/dia em Opus 4.6. Isso é código gerado que precisa de escrutínio."*

**Mais código ≠ melhor software. Quem revisa? Quem testa? Quem mantém?**

---

# O Paradoxo METR (2025)

## Desenvolvedores são 19% MAIS LENTOS com IA

Estudo controlado: 16 devs experientes, 246 tarefas reais

```
  Percepção:  "Sou 20% mais rápido com IA"  ✓
  Realidade:  19% mais lento no tempo total  ✗
```

### Por que isso acontece?

- Tempo gasto revisando e corrigindo código gerado
- Falsa confiança — aceitar sugestões sem entender
- Contexto perdido — a IA não conhece a arquitetura
- Mudança de atividade: de "escrever" para "revisar"

### DORA 2024 confirma:
*Devs individuais fazem 21% mais tarefas, mas métricas organizacionais estagnaram.*

**→ Sem processo, IA amplifica caos, não produtividade.**

---

# Processo como diferencial competitivo

## A IA torna processos MAIS importantes, não menos

```
  SEM processo:   IA → mais código → mais bugs → mais dívida técnica
  COM processo:   IA → código revisado → testes → entrega confiável
```

### O que vamos estudar neste curso:

1. **Frameworks ágeis** — Scrum, XP, Kanban, Lean
2. **DevOps e CI/CD** — automatização do pipeline
3. **Métricas DORA** — medir para melhorar
4. **Mapeamento de Fluxo de Valor** — encontrar gargalos
5. **Topologias de Equipe** — organização que escala
6. **SRE e Plataformas** — operação confiável
7. **IA e processos** — o paradoxo como objeto de estudo

---

# Como funciona este curso

## Sala de aula invertida + Projeto com Scrum

```
📖  ANTES DA AULA (em casa)
    ├── Leia os 2 textos da semana (todos gratuitos)
    └── Assista ao vídeo semanal

🏫  TERÇA-FEIRA (presencial)
    ├── 🧩 Quiz sobre as leituras (10-15 min)
    └── Discussão + atividade prática

🏫  QUINTA-FEIRA (presencial ou online)
    ├── Continuação da prática
    └── Acompanhamento de projeto (a cada sprint)
```

### Projeto integrador:
- Equipes de 3-4 pessoas
- 6 sprints ao longo do semestre
- Vídeos de sprint (foco no PROCESSO, não no produto)
- Stack livre — o importante é demonstrar boas práticas

---

# Avaliação

## Três unidades, nota final = média das três

| Unidade | Componentes |
|---------|-------------|
| **U1** | Sprint 0 (60%) + Quiz de Leitura (40%) |
| **U2** | Prova (50%) + Sprints 1-3 (30%) + Quiz (20%) |
| **U3** | Prova (50%) + Projeto Final (35%) + Proposta de Melhoria (15%) |

### Destaques:
- **Quiz semanal** → incentiva a leitura, substitui listas de exercícios
- **Prova** vale 50% de U2 e U3 (= 1 unidade inteira)
- **Proposta de Melhoria** → VSM + métricas DORA do próprio projeto

---

# Ferramentas

## Tudo gratuito — sem custo para o estudante

| Ferramenta | Uso |
|------------|-----|
| **GitHub** | Repositório + Projects (Kanban) |
| **GitHub Actions** | Pipeline de CI/CD |
| **Docker** | Containerização |
| **Discord** | Comunicação da turma |
| **Google Meet** | Acompanhamentos online |
| **SIGAA** | Entregas oficiais |

### Sincronização com Web II (DIM0547):
- Mesmas datas de sprint
- Mesmo projeto permitido (desde que com entregáveis distintos)

---

# Próximos passos

1. **Ler** os 4 textos da Semana 1 e 2:
   - Royce (1970) — Managing the Development of Large Software Systems
   - Boehm (1988) — A Spiral Model of Software Development and Enhancement
   - Schwaber & Sutherland (2020) — Guia do Scrum (13 pág.)
   - Manifesto Ágil + 12 Princípios
2. **Assistir** ao Vídeo 1 (Scrum)
3. **Formar seu grupo** (3-4 pessoas) até 26/03
4. **Entrar no Discord** da disciplina

### Lembrete:
Na **terça (24/03)** teremos o primeiro **Quiz** sobre as leituras.

---

# Resumo

## O que vimos hoje:

- **Processo de software** = como equipes se organizam para entregar
- **Caso XZ Utils** = sem processo, até infraestrutura crítica é vulnerável
- **Paradoxo da IA** = mais código sem processo = mais problemas
- **Este curso** = ágil-primeiro, orientado por métricas, projeto real

### Links do curso:
- Repositório: `https://github.com/classrooms-fmarquesfilho/ps-2026-1`
- Discord: *[link no SIGAA]*
- Cronograma completo: `docs/CRONOGRAMA.md`
