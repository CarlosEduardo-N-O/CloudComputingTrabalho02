# Plataforma Web de Venda de Ingressos

## Descrição

Aplicação web desenvolvida para gerenciamento de eventos e venda de ingressos, permitindo cadastrar, listar, editar e remover eventos através de uma interface simples e integrada ao banco de dados PostgreSQL.

O sistema foi desenvolvido utilizando Node.js no backend, PostgreSQL para persistência dos dados e Docker para conteinerização da aplicação.

---

# Tecnologias Utilizadas

- Node.js
- Express.js
- PostgreSQL
- Docker
- Docker Compose
- HTML5
- CSS3
- JavaScript

---

# Arquitetura da Aplicação

O projeto utiliza arquitetura multicontainer com Docker Compose:

- Container da aplicação Node.js
- Container do banco PostgreSQL
- Comunicação entre containers via rede Docker
- Persistência de dados utilizando Docker Volumes

---

# Estrutura do Projeto

```text
CloudComputingTrabalho02/
│
├── app/
│   ├── db/
│   │   └── connection.js
│   │
│   ├── public/
│   │   ├── index.html
│   │   ├── style.css
│   │   └── script.js
│   │
│   ├── node_modules/
│   ├── package.json
│   ├── package-lock.json
│   └── server.js
│
├── Dockerfile
├── docker-compose.yml
├── .env
├── README.md
└── .gitattributes

# Funcionalidades

 - Cadastro de eventos
 - Listagem de eventos
 - Edição de eventos
 - Exclusão de eventos

# Persistência de dados em PostgreSQL

# Execução automatizada com Docker Compose

# Como Executar o Projeto
1. Clonar o Repositório
git clone https://github.com/CarlosEduardo-N-O/CloudComputingTrabalho02

2. Acessar a Pasta do Projeto
cd CloudComputingTrabalho02

Exemplo no Windows:
cd C:\Users\carlos.oliveira\OneDrive\Documentos\Cloud Computing\CloudComputingTrabalho02

3. Executar os Containers
docker compose up --build

# Após a execução, a aplicação ficará disponível em:

http://localhost:3000
Portas Utilizadas
Serviço	Porta
Aplicação Node.js	3000
PostgreSQL	5433
Variáveis de Ambiente

Arquivo .env:

PORT=3000

DB_HOST=banco
DB_USER=postgres
DB_PASSWORD=postgres
DB_NAME=ingressos
DB_PORT=5432

# Comandos Docker Úteis

# Subir os Containers
docker compose up

# Reconstruir Containers
docker compose up --build

# Parar os Containers
docker compose down

# Ver Containers em Execução
docker ps

# Ver Volumes Docker
docker volume ls

# Persistência de Dados

Os dados do banco PostgreSQL permanecem armazenados mesmo após a parada dos containers, utilizando Docker Volumes para persistência das informações.

# Rotas da API
- Listar Eventos
- GET /eventos
- Cadastrar Evento
- POST /eventos

# Exemplo:

{
  "nome": "Show Nacional",
  "local": "Rio do Sul",
  "data_evento": "2026-06-10",
  "ingressos": 500
}

# Editar Evento
PUT /eventos/:id

# Excluir Evento
DELETE /eventos/:id

# Objetivo do Projeto

Este projeto foi desenvolvido com foco no aprendizado de:

- Docker e Docker Compose
- Arquitetura multicontainer
- Integração entre Node.js e PostgreSQL
- Desenvolvimento backend com Express.js
- Persistência de dados
- Deploy de aplicações web

# Autor
Carlos Eduardo Nogueira de Oliveira