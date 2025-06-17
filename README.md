# API Express com MongoDB

API RESTful desenvolvida com **Node.js**, **Express** e **MongoDB**. A arquitetura do projeto utiliza **Services**, **Repositories**, **DTOs** e **Middlewares** para uma estrutura organizada e escalável. A autenticação é implementada com JWT e a documentação da API é gerada automaticamente com o Swagger.

***

## Como Executar Localmente

### Pré-requisitos
* **Node.js**: Versão 18.x ou superior.
* **MongoDB**: Uma instância do banco de dados deve estar em execução.

### Passos para Execução

1.  **Clone o repositório:**
    ```bash
    git clone <URL_DO_REPOSITORIO>
    cd <NOME_DO_DIRETORIO>
    ```

2.  **Instale as dependências:**
    ```bash
    npm install
    ```

3.  **Configure as variáveis de ambiente:**
    * Renomeie o arquivo `.env.example` para `.env`.
    * Preencha as variáveis necessárias, como a string de conexão do MongoDB e o segredo do JWT.

4.  **Inicie o servidor:**
    ```bash
    npm start
    ```

O servidor estará disponível em `http://localhost:3000`.

***

## Documentação com Swagger

A documentação completa dos endpoints da API é gerada com o Swagger e pode ser acessada em tempo de execução.

* **URL de acesso:** `http://localhost:3000/api-docs`

***

## Funcionalidades da API

A seguir estão os principais endpoints disponíveis:

### Autenticação (`/auth`)
* **`POST /login`**: Autentica um usuário com e-mail e senha, retornando um token JWT.

### Usuários (`/users`)
* **`GET /`**: Lista todos os usuários.
* **`POST /`**: Cria um novo usuário com senha criptografada.
* **`GET /:id`**: Busca um usuário específico por ID.
* **`PUT /:id`**: Atualiza as informações de um usuário.
* **`DELETE /:id`**: Remove um usuário.
* **`GET /search?name=<nome>`**: Busca usuários por nome.

### Autores (`/authors`)
* **`GET /`**: Lista todos os autores.
* **`POST /`**: Cria um novo autor.
* **`GET /:id`**: Busca um autor por ID.
* **`PUT /:id`**: Atualiza as informações de um autor.
* **`DELETE /:id`**: Remove um autor.
* **`GET /search?name=<nome>`**: Busca autores por nome.

### Postagens (`/posts`)
* **`GET /`**: Lista todas as postagens.
* **`POST /`**: Cria uma nova postagem associada a um autor.
* **`GET /:id`**: Busca uma postagem específica por ID.
* **`PUT /:id`**: Atualiza o conteúdo de uma postagem.
* **`DELETE /:id`**: Remove uma postagem.
* **`GET /search?keyword=<termo>`**: Busca postagens por palavra-chave no título ou na descrição.
