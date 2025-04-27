# Biblioteca-Java

Biblioteca Digital - Sistema de Gerenciamento de Livros
Sobre o Projeto
Este sistema foi desenvolvido para gerenciar o acervo de uma biblioteca de forma simples e eficiente.
Permite cadastrar, listar, editar, remover e consultar livros através de uma API construída com Spring Boot.

🚀 Tecnologias Utilizadas
Java 17+
Spring Boot 3
Spring Data JPA
MySQL (banco de dados relacional)
Maven
Postman (para testar a API)

⚙️ Como Rodar o Projeto
Pré-requisitos
Java 17+
Maven
MySQL Server
IntelliJ IDEA ou outra IDE de sua preferência.


1. Clone o repositório
git clone https://github.com/Th-aylima/Biblioteca-Java.git

2. Configure o Banco de Dados
Crie um banco no seu MySQL chamado biblioteca:

sql
CREATE DATABASE biblioteca;

Em seguida, configure o application.properties ou application.yml:

properties
spring.datasource.url=jdbc:mysql://localhost:3306/biblioteca
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
server.port=8080

3. Compile e Rode o Projeto
No terminal da sua IDE:

./mvnw spring-boot:run

ou clique no botão Run pela IDE.

4. Testando a API
Use o Postman ou Insomnia para fazer as requisições:

Endpoints disponíveis:

Método	     Endpoint    	            Ação
POST	   /api/livros	        Cadastrar novo livro
GET	       /api/livros	        Listar todos os livros
GET	       /api/livros/{id}	    Buscar livro pelo ID
PUT	       /api/livros/{id}	    Atualizar dados de um livro
DELETE	   /api/livros/{id}	    Deletar livro

📋 Estrutura do Projeto

src/
 ├── main/
 │    ├── java/com/example/biblioteca/
 │    │     ├── controller/        (Controladores de API)
 │    │     ├── model/              (Entidade Livro)
 │    │     ├── repository/         (Interface de Repositório JPA)
 │    │     └── BibliotecaApplication.java (Classe principal)
 │    │     
 │    └── resources/
 │          ├── application.properties (Configurações)
 │          └── static/
 └── test/ (Testes unitários)
 
✅ Funcionalidades

Cadastro de novos livros 📚

Listagem completa dos livros disponíveis 📝

Atualização dos dados dos livros 🔄

Remoção de livros do acervo ❌

🧠 Conceitos Aplicados

Programação Orientada a Objetos (POO)

API RESTful

Spring Boot (Framework de criação rápida de aplicações Java)

JPA (Mapeamento objeto-relacional)

Conexão com Banco de Dados MySQL

📢 Observações Finais
As tabelas são criadas automaticamente ao rodar a aplicação pela primeira vez (graças ao spring.jpa.hibernate.ddl-auto=update).
Você pode personalizar o banco de dados e a porta conforme sua necessidade.
O sistema está preparado para receber melhorias como autenticação de usuários, painel de administração, entre outros.

📬 Contato
Caso tenha dúvidas ou sugestões, entre em contato! 🚀
