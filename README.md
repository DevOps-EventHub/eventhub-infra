# EventHub - Infraestrutura

## Descrição do projeto
O EventHub e um sistema web de gerenciamento de eventos.
Este repositório é responsável pela infraestrutura da aplicação, orquestrando os serviços com Docker Compose.

## Objetivo da aplicação
Permitir o gerenciamento de eventos com operações de cadastro, listagem, edição e remoção, com persistência em banco de dados PostgreSQL.

## Tecnologias utilizadas
- Docker
- Docker Compose
- PostgreSQL
- Spring Boot
- React (Vite)

## Pré-requisitos
- Docker Desktop
- Docker Compose (já incluso no Docker Desktop)
- Git

## Instruções para execução
1. Clone os 3 repositórios na mesma pasta pai:
```bash
git clone https://github.com/DevOps-EventHub/eventhub-backend
git clone https://github.com/DevOps-EventHub/eventhub-frontend
git clone https://github.com/DevOps-EventHub/eventhub-infra
```

2. Acesse o repositório de infraestrutura:
```bash
cd eventhub-infra
```

3. Suba os serviços:
```bash
docker compose up --build
```

## Comandos principais
```bash
docker compose up --build
docker compose down
docker compose logs -f
```

## Acessos
- Frontend: http://localhost:5173
- Backend: http://localhost:8081

## Configuração do banco de dados
- Host: `localhost`
- Porta: `5432`
- Database: `eventhub`
- Usuario: `postgres`
- Senha: `postgres`

## Estrutura básica do projeto
- `docker-compose.yml`: define e orquestra os serviços
- `db`: PostgreSQL com volume persistente
- `backend`: API Spring Boot
- `frontend`: aplicação React

## Observacoes
- O banco é inicializado automaticamente ao subir os containers.
- O backend se conecta ao banco pelo serviço `db`.
- Não é necessário instalar PostgreSQL localmente.
- Se a porta `5432` estiver ocupada, ajuste o mapeamento no `docker-compose.yml`.

## Integrantes da equipe
- Samuel Araujo
- José Pereira Neto
- José Mailson
