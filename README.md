# Plataforma de Venda de Ingressos

## Descrição

Aplicação web para cadastro e consulta de eventos, desenvolvida utilizando Node.js, PostgreSQL, Docker e Docker Compose.

---

## Tecnologias Utilizadas

- Node.js
- Express
- PostgreSQL
- Docker
- Docker Compose
- HTML
- CSS
- JavaScript

---

## Arquitetura

A aplicação utiliza arquitetura multicontainer:

- Container da aplicação Node.js
- Container do banco PostgreSQL
- Comunicação via rede Docker
- Persistência utilizando volumes Docker

---

## Estrutura do Projeto

projeto/
├── app/
├── Dockerfile
├── docker-compose.yml
├── README.md
├── .env
└── evidencias/

---

## Como Executar

### Clonar projeto

```bash
git clone URL_DO_REPOSITORIO
```

### Entrar na pasta

```bash
cd projeto
```

### Executar containers

```bash
docker compose up --build
```

---

## Portas Utilizadas

| Serviço | Porta |
|---|---|
| Aplicação | 3000 |
| PostgreSQL | 5432 |

---

## Variáveis de Ambiente

Arquivo `.env`:

```env
PORT=3000

DB_HOST=banco
DB_USER=postgres
DB_PASSWORD=postgres
DB_NAME=ingressos
DB_PORT=5432
```

---

## Docker Compose

Comandos úteis:

### Subir containers

```bash
docker compose up
```

### Parar containers

```bash
docker compose down
```

### Ver containers

```bash
docker ps
```

### Ver volumes

```bash
docker volume ls
```

---

## Persistência

Os dados permanecem salvos utilizando Docker Volumes.

---

## Autor

Carlos Eduardo Nogueira de Oliveira