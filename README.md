🚀 Web Services com Spring Boot + JPA / Hibernate

Projeto desenvolvido durante a Seção 22 – Bônus: Projeto Web Services com Spring Boot e JPA / Hibernate, focado na construção de uma API REST completa em Java utilizando Spring Boot, Spring Data JPA e Hibernate.
O sistema simula um backend de e-commerce, contendo gerenciamento de usuários, produtos, pedidos, categorias e pagamentos.

🧰 Tecnologias Utilizadas
☕ Java 25
🌱 Spring Boot 4.0.4
🗄 Spring Data JPA
🔗 Hibernate
📦 Maven
🧪 H2 Database (ambiente de teste)
🌐 REST API
📄 JSON
🧠 Tratamento de exceções customizado
📂 Estrutura do Projeto
src/main/java/com/educandoweb/course

├── config
│   └── TestConfig.java

├── entities
│   ├── Category.java
│   ├── Order.java
│   ├── OrderItem.java
│   ├── Payment.java
│   ├── Product.java
│   └── User.java

├── entities.enums
│   └── OrderStatus.java

├── entities.pk
│   └── OrderItemPK.java

├── repositories
│   ├── CategoryRepository.java
│   ├── OrderRepository.java
│   ├── OrderItemRepository.java
│   ├── ProductRepository.java
│   └── UserRepository.java

├── resources (Controllers)
│   ├── CategoryResource.java
│   ├── OrderResource.java
│   ├── ProductResource.java
│   └── UserResource.java

├── services
│   ├── CategoryService.java
│   ├── OrderService.java
│   ├── ProductService.java
│   └── UserService.java

├── services.exceptions
│   ├── DatabaseException.java
│   └── ResourceNotFoundException.java

└── resources.exceptions
    ├── ResourceExceptionHandler.java
    └── StandardError.java
    
🧱 Arquitetura Utilizada
O projeto segue a arquitetura em camadas:
Controller (Resource)
        ↓
Service
        ↓
Repository
        ↓
Database

📌 Camadas
Resource / Controller
Responsável pelas rotas REST
Recebe e responde requisições HTTP

Service
Contém a lógica de negócio

Repository
Interface de acesso ao banco de dados
Utiliza Spring Data JPA

Entities
Representação das tabelas do banco
📊 Modelo de Domínio

O sistema possui as seguintes entidades principais:
👤 User
📦 Product
🗂 Category
🧾 Order
💰 Payment
📑 OrderItem

Relacionamentos incluem:
ManyToMany
OneToMany
ManyToOne
🌐 Endpoints da API
👤 Usuários
GET /users
GET /users/{id}
POST /users
PUT /users/{id}
DELETE /users/{id}
📦 Produtos
GET /products
GET /products/{id}
🗂 Categorias
GET /categories
GET /categories/{id}
🧾 Pedidos
GET /orders
GET /orders/{id}
⚠️ Tratamento de Exceções

O projeto implementa tratamento de erros usando:

ResourceNotFoundException
DatabaseException

Com um handler global:
ResourceExceptionHandler
Retornando respostas padronizadas:

{
  "timestamp": "2025-01-01T10:00:00Z",
  "status": 404,
  "error": "Resource not found",
  "message": "Entity not found",
  "path": "/users/10"
}

⚙️ Configuração de Ambientes

Arquivos de configuração:

application.properties
application-dev.properties
application-test.properties

Perfis utilizados:
test
dev

🧪 Banco de Dados de Teste
O projeto utiliza H2 Database para ambiente de teste.
Console H2:
http://localhost:8080/h2-console

🎓 Créditos
Este projeto foi desenvolvido como parte dos estudos no curso Java COMPLETO Programação Orientada a Objetos + Projetos, ministrado pelo professor Nelio Alves na plataforma Udemy.
O projeto tem finalidade educacional e foi utilizado para aplicar conceitos de Java, Programação Orientada a Objetos, Spring Boot, JPA e Hibernate na construção de uma API REST.
