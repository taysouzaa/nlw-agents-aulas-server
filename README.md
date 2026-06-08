# NLW Agents — Servidor de Aulas

> Servidor de agentes de IA desenvolvido durante o NLW Agents da Rocketseat, com busca semântica por vetores e API REST.

![Status](https://img.shields.io/badge/status-concluído-22c55e)
![TypeScript](https://img.shields.io/badge/TypeScript-Node.js-3178c6?logo=typescript)
![PostgreSQL](https://img.shields.io/badge/DB-PostgreSQL%2Fpgvector-336791?logo=postgresql)
![Docker](https://img.shields.io/badge/infra-Docker-2496ED?logo=docker)
![License](https://img.shields.io/badge/license-MIT-green)

## Visão do Projeto

O **NLW Agents** é um servidor de agentes de IA construído durante o evento **NLW Agents da Rocketseat**. O projeto implementa uma API REST com busca semântica baseada em vetores (pgvector), permitindo que agentes de IA consultem e respondam perguntas sobre conteúdo de aulas.

### O que o sistema resolve

- Permite busca semântica em conteúdo de aulas via embeddings vetoriais.
- Expõe endpoints REST para integração com agentes de IA.
- Containeriza banco de dados com Docker para setup rápido.

## O Que Foi Desenvolvido

### 1. API REST com Fastify
- Endpoints para criação, consulta e busca de conteúdo de aulas.
- Validação de dados com **Zod**.
- Roteamento modular e type-safe.

### 2. Banco de Dados Vetorial
- PostgreSQL com extensão **pgvector** para armazenamento de embeddings.
- **Drizzle ORM** para queries type-safe e migrations.
- Docker Compose para subir o banco localmente com um comando.

### 3. Qualidade de Código
- TypeScript nativo (experimental strip types — sem transpilação).
- **Biome** para linting e formatação consistente.
- Arquivo `client.http` para testes manuais de endpoints.

## Stack Técnica

- **Backend:** Node.js (TypeScript nativo), Fastify
- **Banco:** PostgreSQL + pgvector, Drizzle ORM
- **Validação:** Zod
- **Infra:** Docker, Docker Compose
- **Qualidade:** Biome

## Estrutura do Projeto

```text
.
├─ src/                   ← código-fonte principal
├─ docker/                ← configurações Docker
├─ docker-compose.yml     ← banco de dados local
├─ drizzle.config.ts      ← configuração de migrations
├─ client.http            ← testes de endpoints
├─ biome.jsonc            ← linting/formatação
├─ package.json
└─ tsconfig.json
```

## Como Executar

```bash
# Subir banco de dados
docker-compose up -d

# Instalar dependências e rodar
npm install
npm run db:migrate
npm run dev
```

## Licença

MIT — veja [LICENSE](./LICENSE)