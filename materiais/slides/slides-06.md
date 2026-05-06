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

# Pipeline na prática: Actions + Docker
## Processos de Software — Sprint 2 (prática)

**Prof. Fernando** · UFRN · 2026.1

---

# De onde paramos

Aula passada: **teoria** de DevOps.

| Vimos | Hoje |
|---|---|
| CALMS, 3 caminhos, DORA | Mão na massa |
| "CI é integrar diariamente" | Escrever um `ci.yml` que roda |
| "Docker garante reprodutibilidade" | Escrever um `Dockerfile` que faz o _build_ |
| "Pipeline como filtro" | Ver o filtro funcionando (e quebrando) |

> Objetivo de hoje: **se o lint passa e os testes passam no CI, está tudo pronto para a Sprint 2**.

---

# Plano da aula

1. Anatomia de um pipeline GitHub Actions <span class="tag">~10 min</span>
2. Dockerfile multi-stage: por que e como <span class="tag">~10 min</span>
3. **Prática guiada no Codespaces** <span class="tag">~30 min</span>
   - Etapa 1: workflow de CI
   - Etapa 2: Dockerfile
   - Etapa 3: docker-compose
4. Dicas para o vídeo de 8min <span class="tag">~5 min</span>

---

# GitHub Actions: vocabulário mínimo

| Termo | O que é |
|---|---|
| **Workflow** | Arquivo YAML em `.github/workflows/`. Um pipeline. |
| **Event** | O que dispara o workflow (`push`, `pull_request`, ...) |
| **Job** | Conjunto de passos que rodam numa mesma máquina virtual |
| **Step** | Um comando ou uso de uma `action` reutilizável |
| **Runner** | A VM que executa o job (`ubuntu-latest` é o padrão) |
| **Action** | Bloco reutilizável (ex: `actions/checkout@v4`) |

> Vamos escrever um arquivo YAML que descreve uma sequência de comandos que rodam numa VM Ubuntu temporária no GitHub.

---

# Anatomia: o `ci.yml` mais simples possível

```yaml
name: CI                              # nome que aparece na aba Actions

on:                                   # quando rodar
  push:
    branches: [main]
  pull_request:

jobs:
  test:                               # nome do job (livre)
    runs-on: ubuntu-latest            # qual VM
    steps:
      - uses: actions/checkout@v4     # baixa o código do repo
      - uses: actions/setup-python@v5 # instala Python
        with:
          python-version: '3.12'
      - run: pip install -r requirements.txt -r requirements-dev.txt
      - run: pytest                   # roda os testes
```

**É isso.** Cinco passos lógicos: dispara → VM sobe → baixa código → instala stack → roda teste.

---

# O que torna um pipeline "bom"

Não é complexidade. É **cobertura dos pontos de falha**:

| Etapa | O que ela pega |
|---|---|
| `pip install` | Dependência quebrada ou conflito |
| `ruff check` | Lint: imports não usados, código morto, estilo |
| `pytest` | Comportamento quebrado |
| `pytest --cov` | Código sem cobertura de teste |
| `mypy` | Erros de tipo (opcional, para projetos tipados) |
| `docker build` | Imagem não builda |

> Cada etapa é um **filtro**. Falhou em qualquer uma → não passa adiante.

---

# Cache: do "lento" ao "rápido"

Sem cache: cada build baixa todas as dependências de novo. Pode levar 1-2 min.

```yaml
- uses: actions/setup-python@v5
  with:
    python-version: '3.12'
    cache: 'pip'                      # ← uma linha mais.
```

Resultado típico: build cai de 90s para 20s.

> **Lead time** é uma das métricas DORA. Cache no CI **mexe diretamente** nessa métrica.

---

# Dockerfile: por que multi-stage?

**Dockerfile ingênuo (NÃO façam isso)**:

```dockerfile
FROM python:3.12
COPY . .
RUN pip install -r requirements.txt
CMD ["python", "-m", "app.main"]
```

Problemas:
- Imagem final ~1 GB (Python "completo" + pip cache + ferramentas de build)
- Roda como `root` (sem segurança em camadas)
- Copia `tests/`, `.git/`, etc. para produção
- Reinstala tudo a cada mudança no código

---

# Dockerfile multi-stage

```dockerfile
# Stage 1: builder — instala dependências
FROM python:3.12-slim AS builder
WORKDIR /build
COPY requirements.txt .
RUN pip install --user --no-cache-dir -r requirements.txt

# Stage 2: runtime — só o necessário
FROM python:3.12-slim
RUN useradd --create-home app
USER app
WORKDIR /home/app
COPY --from=builder --chown=app:app /root/.local /home/app/.local
COPY --chown=app:app app/ ./app/
ENV PATH=/home/app/.local/bin:$PATH
CMD ["python", "-m", "app.main"]
```

Imagem final: **~150 MB**, rodando como usuário `app`.

> Lean aplicado ao CI: **eliminar desperdício** otimizando e provendo mais segurança no processo de automação de build.

---

# Por que `--user` e copiar `/root/.local`?

```dockerfile
RUN pip install --user --no-cache-dir -r requirements.txt
# ...
COPY --from=builder --chown=app:app /root/.local /home/app/.local
```

- `--user`: instala em `~/.local` em vez de site-packages global. Tudo num lugar só.
- `--no-cache-dir`: além de instalar em `~/.local`, o pip guarda uma cópia dos wheels em `~/.cache/pip` para acelerar futuras instalações. Numa imagem Docker isso nunca é usado (o `pip install` só roda uma vez no build), então o cache fica ocupando espaço à toa. `--no-cache-dir` desliga essa cópia. Tipicamente economiza 30-50MB.
- A stage final copia **apenas** `~/.local` — sem pip, sem ferramentas de build, sem cache.

> A stage de build pode ter o que for preciso. A stage de runtime tem **só o mínimo para rodar**.

---

# E rodar como root? Por que não?

```dockerfile
RUN useradd --create-home app
USER app
```

**Defesa em profundidade**: se a aplicação for comprometida (RCE via lib vulnerável, p.ex.), o atacante fica preso num usuário sem privilégios.

Sem isso: o atacante **é root** dentro do container — pode escrever em qualquer lugar, instalar ferramentas, escalar privilégios.

> É uma linha de proteção. Não é tudo, mas é gratuito e funciona.

---

# docker-compose: orquestrar serviços

Sua API quase nunca roda sozinha. Tem banco, cache, fila...

```yaml
services:
  api:
    build: .
    ports: ["8080:8080"]
    environment:
      DATABASE_URL: postgresql://app:app@db:5432/app
    depends_on:
      db:
        condition: service_healthy

  db:
    image: postgres:16-alpine
    environment:
      POSTGRES_USER: app
      POSTGRES_PASSWORD: app
      POSTGRES_DB: app
    healthcheck:
      test: ["CMD-SHELL", "pg_isready -U app"]
      interval: 5s
```

Um comando: `docker compose up`. Um comando para derrubar tudo: `docker compose down`.

---

# Por que `healthcheck` + `depends_on`?

Sem healthcheck:

```
api sobe → tenta conectar no banco → banco ainda inicializando → CRASH
```

Com healthcheck:

```
db sobe → healthcheck "pg_isready" passa →
                                     → api sobe → conecta com sucesso
```

> `depends_on` simples só espera o **container** subir. Com `condition: service_healthy`, espera o **serviço** estar pronto. Diferença sutil, mas é o que separa "funciona às vezes" de "funciona sempre".

---

# Onde Codespaces entra

GitHub Codespaces = **VM Ubuntu pronta no navegador**, com Docker-in-Docker.

| Vocês não precisam | Codespaces dá |
|---|---|
| Instalar Docker no PC do lab | Já vem |
| Permissão de admin | Roda no GitHub |
| Stack Python local | `devcontainer` configura |

> **Atenção**: a cota gratuita do Codespaces é generosa, mas finita. Parem o codespace quando não estiverem usando: aba Codespaces → `...` → **Stop codespace**.

---

# Prática agora — 3 etapas

**Repo base**: *(link enviado no Discord)* — forkar para a conta do time.

| Etapa | Tempo | Resultado |
|---|---|---|
| **1** — Workflow de CI | 10 min | Pipeline rodando, badge verde |
| **2** — Dockerfile multi-stage | 10 min | Imagem buildando local e no CI |
| **3** — docker-compose | 10 min | App + Postgres rodando juntos |

Cada etapa tem um arquivo `STEP-N.md` no repo com as instruções.

> **Vamos quebrar coisas de propósito.** É a melhor forma de entender o que cada filtro pega.

---

# Sobre o vídeo de 8min

Vocês vão **gravar a tela** mostrando a Sprint 2. Hoje vocês geram a matéria-prima.

Roteiro sugerido (8 min):

| Parte | Tempo | Conteúdo |
|---|---|---|
| Pipeline em ação | 2 min | Push → CI roda → verde |
| Quebrar de propósito | 1 min | Push com teste falhando → CI vermelho |
| Docker rodando | 2 min | `docker compose up`, app responde |
| Métricas DORA | 2 min | Dois números + interpretação |
| Reflexão | 1 min | O que mudou no fluxo do time? |

> **Não narrem o YAML linha por linha.** Mostrem o **efeito**. O artefato fala por si.

---

# Métricas DORA: como coletar (mínimo viável)

Vocês não precisam de dashboard. Precisam de **dois números** pelo menos (podem coletar mais se conseguirem e no trabalho isso será convertido em um pequeno bônus).

**Frequência de deploy** *(proxy: merges em main)*:
```bash
git log --since="2 weeks ago" --oneline main | wc -l
```

**Lead time** *(commit → merge em main)*:
- Anotem na descrição do PR: data do primeiro commit e data do merge.
- Calculem a média.

> Não _mascarar_ um resultado só porque ele seja aparentemente **ruim**. Peguem o número **real** e elaborem em grupo o que será feito para melhorar. Isso é **DORA**, e tem relação com a cultura de **melhoria contínua** que vimos no Lean e no Scrum.

---

# Checklist antes de ir embora

Sprint 2 entrega <span class="tag">prazo: 19/05 23:59</span>:

- [ ] `.github/workflows/ci.yml` rodando verde
- [ ] `Dockerfile` multi-stage compila
- [ ] `docker-compose.yml` sobe app + dependência
- [ ] `METRICS.md` com 2 métricas DORA reais
- [ ] Retrospectiva da Sprint 2 documentada
- [ ] Vídeo 8 min gravado e linkado

> Se até o fim da prática de hoje vocês tiverem os três primeiros, **a sprint está 70% feita**.

---

# Referências da aula

- GitHub Actions docs — [docs.github.com/actions](https://docs.github.com/actions)
- Docker multi-stage builds — [docs.docker.com/build/building/multi-stage](https://docs.docker.com/build/building/multi-stage/)
- Compose specification — [compose-spec.io](https://compose-spec.io/)
- DORA — *Four Keys* — [dora.dev/guides/dora-metrics-four-keys](https://dora.dev/guides/dora-metrics-four-keys/)
- Codespaces docs — [docs.github.com/codespaces](https://docs.github.com/codespaces)
