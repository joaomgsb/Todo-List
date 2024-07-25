
# Todo List API

Este projeto é uma API para controle de Tasks (Lista de Tarefas). A API permite criar, ler, atualizar e deletar tarefas, além de realizar a autenticação de usuários utilizando JWT.

## Funcionalidades

- Criação de rotas HTTP
- Recebimento e validação de parâmetros
- Integração com banco de dados
- Autenticação com JWT utilizando Spring Security
- Deploy na plataforma Render

## Tecnologias Utilizadas

- **Java**
- **Spring Boot**
- **Spring Security**
- **JWT**
- **Banco de dados H2**
- **Plataforma de deploy Render**

## Como Executar o Projeto

### Pré-requisitos

- Java 11 ou superior
- Maven

### Passos

1. Clone o repositório:

    ```bash
    git clone https://github.com/seu-usuario/todo-list-api.git
    cd todo-list-api
    ```

2. Execute o projeto:

    ```bash
    mvn spring-boot:run
    ```

### Configuração do Banco de Dados

O projeto está configurado para usar o banco de dados em memória H2. A configuração pode ser encontrada no arquivo `application.properties`:

```properties
spring.application.name=todolist
spring.datasource.url=jdbc:h2:mem:todolist
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=admin
spring.datasource.password=admin
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.h2.console.enabled=true
```

## Acessando o Console H2

Para acessar o console do banco de dados H2, navegue até `http://localhost:8080/h2-console` e use as credenciais configuradas (`admin` / `admin`).

## Endpoints

A API possui os seguintes endpoints:

- **GET** `/tasks` - Lista todas as tarefas
- **GET** `/tasks/{id}` - Obtém uma tarefa pelo ID
- **POST** `/tasks` - Cria uma nova tarefa
- **PUT** `/tasks/{id}` - Atualiza uma tarefa pelo ID
- **DELETE** `/tasks/{id}` - Deleta uma tarefa pelo ID

## Autenticação

A API utiliza JWT para autenticação. Para acessar os endpoints protegidos, você deve incluir o token JWT no cabeçalho das requisições.

## Deploy

O deploy foi realizado na plataforma Render. Para acessar a aplicação em produção, utilize a seguinte URL: [URL da sua aplicação na Render]

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests.


