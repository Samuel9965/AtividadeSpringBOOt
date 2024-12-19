# API de Produtos


Esta é uma API RESTful para gerenciar produtos em um sistema de estoque. A API permite realizar operações de CRUD (Criar, Ler, Atualizar e Deletar) em produtos.


## Sumário


- [Descrição do Projeto](#descrição-do-projeto)

- [Tecnologias Utilizadas](#tecnologias-utilizadas)

- [Configuração do Ambiente](#configuração-do-ambiente)

- [Executando o Projeto](#executando-o-projeto)

- [Endpoints](#endpoints)

- [Exemplos de Uso via cURL](#exemplos-de-uso-via-curl)

- [Contribuições](#contribuições)


## Descrição do Projeto


Este projeto é uma API para gerenciar produtos, permitindo que os usuários realizem operações de CRUD. A tabela `produtos` contém informações sobre cada produto, incluindo um identificador único, nome, descrição, preço e quantidade disponível em estoque.


## Tecnologias Utilizadas


- **Java 17**: Linguagem de programação utilizada.

- **Spring Boot**: Framework para desenvolvimento de aplicações Java.

- **Spring Data JPA**: Para interação com o banco de dados.

- **PostgreSQL**: Sistema de gerenciamento de banco de dados utilizado (pode ser adaptado para MySQL).

- **Flyway**: Para versionamento do banco de dados.

- **cURL**: Para testar os endpoints da API.


## Configuração do Ambiente


1. **Clone o repositório:**

   ```bash

   git clone <https://github.com/Samuel9965/AtividadeSpringBOOt.git>

   cd <AtividadeSpringBOOt.git>

    Configure o banco de dados:
        Crie um banco de dados no PostgreSQL (ou MySQL) chamado estoque_db.
        Execute o script SQL para criar a tabela produtos e inserir dados de exemplo.

    Configuração do application.properties:
        Navegue até src/main/resources e configure o arquivo application.properties com as credenciais do seu banco de dados.

    Dependências:
        Certifique-se de que as dependências necessárias estão no arquivo pom.xml (para Maven) ou build.gradle (para Gradle).

Executando o Projeto

    Compile e execute a aplicação:
        Utilize sua IDE (como IntelliJ IDEA) ou execute o seguinte comando no terminal:

    bash

    ./mvnw spring-boot:run

    Acesse a API:
        A API estará disponível em http://localhost:8080.

Endpoints
1. Criar um Produto (POST)

Endpoint: POST /api/produtos

Descrição: Cria um novo produto.
2. Listar Todos os Produtos (GET)

Endpoint: GET /api/produtos

Descrição: Recupera todos os produtos.
3. Obter um Produto por ID (GET)

Endpoint: GET /api/produtos/{id}

Descrição: Recupera um produto específico pelo ID.
4. Atualizar um Produto (PUT)

Endpoint: PUT /api/produtos/{id}

Descrição: Atualiza um produto existente.
5. Deletar um Produto (DELETE)

Endpoint: DELETE /api/produtos/{id}

Descrição: Remove um produto pelo ID.
Exemplos de Uso via cURL
Criar um Produto (POST)

bash

curl -X POST http://localhost:8080/api/produtos \

-H "Content-Type: application/json" \

-d '{

    "nome": "Produto D",

    "descricao": "Descrição do Produto D",

    "preco": 49.99,

    "quantidade": 10

}'

Listar Todos os Produtos (GET)

bash

curl -X GET http://localhost:8080/api/produtos

Obter um Produto por ID (GET)

bash

curl -X GET http://localhost:8080/api/produtos/1

Atualizar um Produto (PUT)

bash

curl -X PUT http://localhost:8080/api/produtos/1 \

-H "Content-Type: application/json" \

-d '{

    "nome": "Produto A Atualizado",

    "descricao": "Descrição atualizada do Produto A",

    "preco": 24.99,

    "quantidade": 80

}'

Deletar um Produto (DELETE)

bash

curl -X DELETE http://localhost:8080/api/produtos/1
