# Processos de Software

**Universidade Federal do Rio Grande do Norte**  
**Departamento de Informática e Matemática Aplicada**  
**Bacharelado em Engenharia de Software**  
**Prof. Fernando Figueira | 2026.1**

---

## Sobre o Curso

Este repositório contém todo o material didático para a disciplina de Processos de Software, com foco em **métodos ágeis, práticas DevOps e melhoria contínua baseada em métricas**.

### Metodologia: Sala de Aula Invertida + PBL

```
📖 ANTES DA AULA
   └── Leia os 2 textos indicados para a semana
   └── Assista ao vídeo semanal

🏫 TERÇA-FEIRA (presencial, 10:30-12:00)
   └── 🧩 Quiz presencial sobre as leituras (10-15 min)
   └── Revisão rápida + Esclarecimento de dúvidas
   └── Atividade prática ou discussão guiada

🏫 QUINTA-FEIRA (presencial ou online)
   └── Continuação da prática / Discussão
   └── Acompanhamento de projeto a cada final de sprint (via Google Meet)
```

**Documentos importantes:**

- [Plano de curso](docs/PLANO_DE_CURSO.md)
- [Cronograma detalhado](docs/CRONOGRAMA.md)
- [Critérios de avaliação](docs/AVALIACAO.md)

**Por que essa metodologia?**  
- Leituras de artigos e guias da indústria e academia
- Quiz no início da aula incentiva a leitura e prepara a discussão
- Mais tempo para prática e discussão em sala
- Vivência real de processos ágeis no projeto integrador

### O que torna este curso diferente

1. **Processo como produto**: a qualidade do processo é tão importante quanto o software produzido
2. **Métricas DORA**: equipes coletam e analisam métricas do próprio projeto
3. **Leituras fundamentais**: contato direto com artigos seminais e documentos de referência
4. **Reflexão sobre IA e Processos**: análise crítica de como IA impacta processos de software

### Visão Geral do Conteúdo

```
Semana 1:      Fundamentos — por que processos importam + modelos de ciclo de vida
Semanas 2-4:   Frameworks ágeis — Scrum, XP, Lean, Kanban
Semanas 5-6:   DevOps — cultura, CI/CD, containerização
Semanas 7-8:   Medição — métricas DORA, Value Stream Mapping
Semana 9:      Qualidade de processos + Revisão
Semana 10:     Prova Escrita (12/05)
Semanas 11-12: Organizações — Topologias de Equipe, Engenharia de Plataformas, SRE
Semana 13:     IA e Processos — o Paradoxo da Produtividade
Semana 14:     Padrões, maturidade e melhoria contínua
Semanas 15-16: Apresentações finais + Encerramento
```

---

## Informações do Curso

- **Horário**: Terças e Quintas, 10:30 às 12:00 (M56)
- **Modalidade**: Presencial com Sala de Aula Invertida
- **Carga horária**: 60 horas
- **Período**: 17/03/2026 a 11/07/2026

### Discord da Disciplina

Link disponível na turma virtual do SIGAA.

Canais principais:
- `#anuncios` — Avisos importantes do professor
- `#duvidas-u1`, `#duvidas-u2`, `#duvidas-u3` — Dúvidas por unidade
- `#projeto` — Discussões sobre o projeto integrador
- `#procurando-grupo` — Para formar equipes
- `#recursos` — Links úteis, artigos, vídeos complementares

### Outros Canais

- **YouTube**: Playlist de vídeos semanais (link no Discord)
- **Google Meet**: Para acompanhamentos online de projeto
- **SIGAA**: Entregas oficiais e notas
- **GitHub**: Repositórios de projeto

---

## Estrutura do Repositório

```
.
├── README.md                    # Este arquivo
├── docs/
│   ├── PLANO_DE_CURSO.md       # Programa completo
│   ├── CRONOGRAMA.md           # Cronograma detalhado com datas
│   ├── AVALIACAO.md            # Critérios de avaliação
│   └── REFERENCIAS.md          # Bibliografia e recursos
└── materiais/
    ├── slides/                  # Slides das aulas (quando aplicável)
    └── templates/
        ├── proposta-projeto.md  # Template para proposta de projeto
        ├── sprint-review.md     # Template para vídeo de sprint
        └── vsm-template.md     # Template para Value Stream Map
```

---

## Pré-requisitos

### Conhecimentos Esperados

1. Experiência com programação em alguma linguagem
2. Familiaridade com Git e GitHub

### Ferramentas Necessárias

```bash
# Git
git --version

# Docker (necessário a partir da Semana 7)
docker --version

# Uma conta no GitHub com acesso ao GitHub Projects
```

---

## Projeto Integrador

O curso é centrado em um **projeto em equipe** desenvolvido ao longo do semestre usando Scrum. A diferença fundamental: nesta disciplina, **o processo é o foco principal da avaliação**, não apenas o produto final.

### O que a equipe entrega

- **6 vídeos de sprint** documentando o progresso (processo + produto)
- **Quadro Kanban** mantido ao longo do semestre no GitHub Projects
- **Métricas DORA** coletadas do próprio projeto
- **Value Stream Map** do fluxo de entrega da equipe
- **Proposta de melhoria de processo** baseada em dados
- **Apresentação final** com reflexão sobre o processo vivido

### Stack tecnológico

Livre! A equipe pode usar qualquer linguagem e/ou framework. O importante é que o projeto permita demonstrar práticas de processo (CI/CD, testes, revisão de código).

> **Cursando Web II simultaneamente?** Você pode usar o mesmo projeto em ambas as disciplinas. Os entregáveis são distintos: Processos foca no **processo** (métricas, retrospectivas, VSM); Web foca no **produto** (funcionalidades, código, arquitetura).

---

## Avaliação

A nota final é a **média aritmética das 3 unidades**:

```
Nota Final = (U1 + U2 + U3) / 3
```

| Unidade | Componentes |
|---------|-------------|
| **U1** | Sprint 0 (60%) + Quiz de Leitura (40%) |
| **U2** | **Prova Escrita (50%)** + Sprints 1-3 (30%) + Quiz de Leitura (20%) |
| **U3** | **Prova Escrita (50%)** + Projeto Final (35%) + Proposta de Melhoria (15%) |

A **Prova Escrita** (12/05) vale 50% de U2 e 50% de U3 — equivalendo a uma unidade inteira. Cobre o conteúdo das Unidades 1 e 2, com consulta a 1 folha A4 manuscrita.

Detalhes completos em [docs/AVALIACAO.md](docs/AVALIACAO.md).

---

## Licença

Este material é disponibilizado como **Recurso Educacional Aberto (REA)** sob a licença [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).

Você pode compartilhar e adaptar este material para fins não comerciais, desde que atribua crédito e distribua sob a mesma licença.