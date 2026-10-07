# Lista de Tarefas API

API RESTful para gerenciamento de usuários e tarefas, desenvolvida em Node.js com Express e Prisma ORM conectado ao banco de dados PostgreSQL. Inclui documentação interativa com Swagger.

---

## 🚀 Tecnologias Utilizadas

- **[Node.js](https://nodejs.org/)** - Ambiente de execução JavaScript
- **[Express](https://expressjs.com/)** - Framework web minimalista e flexível
- **[Prisma ORM](https://www.prisma.io/)** - Mapeamento objeto-relacional para PostgreSQL
- **[PostgreSQL](https://www.postgresql.org/)** - Banco de dados relacional
- **[Swagger UI Express](https://github.com/scottie1984/swagger-ui-express)** / **[Swagger Autogen](https://swagger-autogen.github.io/)** - Documentação interativa da API
- **[Bcrypt](https://github.com/kelektiv/node.bcrypt.js)** - Criptografia de senhas
- **[CORS](https://github.com/expressjs/cors)** - Habilitação de Cross-Origin Resource Sharing

---

## 📋 Pré-requisitos

- Node.js (versão 18 ou superior recomendada)
- Gerenciador de pacotes npm
- Instância do PostgreSQL em execução

---

## 🔧 Instalação e Execução

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/luan-Silva-Dev-0fc/lista-tarefa-api.git
   cd lista-tarefa-api
   ```

2. **Instale as dependências:**
   ```bash
   npm install
   ```

3. **Configure as variáveis de ambiente:**
   Copie o arquivo `.env.example` para `.env` e preencha a URL de conexão do PostgreSQL:
   ```bash
   cp .env.example .env
   ```

4. **Gere os clientes e migrações do Prisma:**
   ```bash
   npx prisma generate
   ```

5. **Inicie o servidor em modo de desenvolvimento:**
   ```bash
   npm run dev
   ```

O servidor estará rodando em `http://localhost:8000`.

---

## 📖 Documentação da API (Swagger)

Acesse a documentação interativa diretamente pelo navegador:
- [http://localhost:8000/docs](http://localhost:8000/docs)

Para atualizar a documentação com o Swagger Autogen:
```bash
npm run swagger
```

---

## 📌 Rotas Principais

### Autenticação & Geral
| Método | Endpoint | Descrição |
|---|---|---|
| `GET` | `/` | Redireciona para `/docs` |
| `POST` | `/login` | Autenticação do usuário |
| `GET` | `/docs` | Interface do Swagger UI |

### Usuários
| Método | Endpoint | Descrição |
|---|---|---|
| `GET` | `/usuarios` | Lista todos os usuários |
| `POST` | `/usuarios` | Cria um novo usuário |
| `PUT` | `/usuarios/:id` | Atualiza um usuário |
| `DELETE` | `/usuarios/:id` | Remove um usuário |

### Tarefas
| Método | Endpoint | Descrição |
|---|---|---|
| `GET` | `/tarefas` | Lista tarefas cadastradas |
| `POST` | `/tarefas` | Cria uma nova tarefa vinculada a um usuário |
| `PUT` | `/tarefas/:id` | Atualiza uma tarefa |
| `DELETE` | `/tarefas/:id` | Remove uma tarefa |
