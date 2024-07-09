# travel-planner-app

Trip Planner Application
Este é um projeto para um aplicativo de planejamento de viagens, desenvolvido utilizando Java com Spring Boot e Hibernate para persistência de dados.

Pré-requisitos
Certifique-se de ter as seguintes ferramentas instaladas:

JDK 11 ou superior
Maven 3.x
IDE Java 
Configuração do Banco de Dados
O aplicativo utiliza um banco de dados relacional. Configure as propriedades de conexão no arquivo application.properties.

Exemplo de configuração para banco de dados H2 em memória:

properties
Copiar código
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=password
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.h2.console.enabled=true
Como Executar
Clone este repositório.
Importe o projeto na sua IDE.
Configure as propriedades do banco de dados conforme necessário.
Execute a aplicação.
Acesse http://localhost:8080 para interagir com o aplicativo.

Endpoints
Criar Nova Viagem
URL: /trips
Método: POST
Payload:
json

{
  "destination": "Nome do destino",
  "starts_at": "2024-07-10T08:00:00",
  "ends_at": "2024-07-15T18:00:00",
  "emails_to_invite": ["email1@example.com", "email2@example.com"],
  "owner_email": "owner@example.com",
  "owner_name": "Nome do proprietário"
}

Estrutura do Projeto
com.planner.planner.trip.Trip: Entidade JPA para representar uma viagem.
com.planner.planner.trip.TripRepository: Interface de repositório para operações de banco de dados.
com.planner.planner.trip.TripController: Controlador REST para gerenciar requisições relacionadas a viagens.
com.planner.planner.trip.TripRequestPayload: DTO para receber dados de requisição de criação de viagem.
