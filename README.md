# Criando Aplicação Fullstack do Zero com Java Spring e React

Bem-vindo ao tutorial "Criando Aplicação Fullstack do Zero com Java Spring e React". Esta é a **Parte 1** da série, onde abordaremos o desenvolvimento do backend utilizando **Java Spring Boot** e **PostgreSQL**.

## Visão Geral

Neste tutorial, vamos construir o backend de uma aplicação fullstack com Java Spring Boot. A aplicação será uma API RESTful que servirá dados para o frontend, que será desenvolvido na Parte 2 usando React.

## Objetivos

- Configurar um projeto Spring Boot com PostgreSQL.
- Criar uma API RESTful com endpoints básicos.
- Integrar o Spring Data JPA para persistência de dados.
- Testar a aplicação usando ferramentas como Postman.

## Pré-requisitos

Antes de começar, você deve ter:

- [Java JDK 17+](https://www.oracle.com/java/technologies/javase-downloads.html)
- [Maven](https://maven.apache.org/download.cgi) (ou [Gradle](https://gradle.org/install/), se preferir)
- [PostgreSQL](https://www.postgresql.org/download/) (instalado e em execução)
- [Postman](https://www.postman.com/downloads/) (para testar a API)

## Configuração do Projeto

1. **Criar um novo projeto Spring Boot**

   Utilize o [Spring Initializr](https://start.spring.io/) para criar um novo projeto Spring Boot com as seguintes opções:

   - Project: Maven Project (ou Gradle Project)
   - Language: Java
   - Spring Boot: [Versão estável mais recente]
   - Dependencies: Spring Web, Spring Data JPA, PostgreSQL Driver

   Clique em "Generate" para baixar o projeto.

2. **Importar o Projeto**

   Descompacte o arquivo baixado e importe-o para sua IDE favorita (por exemplo, IntelliJ IDEA ou Eclipse).

3. **Configurar o Banco de Dados**

   Abra o arquivo `src/main/resources/application.properties` e configure a conexão com o PostgreSQL:

   ```properties
   spring.datasource.url=jdbc:postgresql://localhost:5432/seu_banco
   spring.datasource.username=seu_usuario
   spring.datasource.password=sua_senha
   spring.jpa.hibernate.ddl-auto=update
   spring.jpa.show-sql=true
   spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
