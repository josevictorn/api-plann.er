# Travel Planner API

API para ajudar usuários a organizar viagens de trabalho ou lazer. Os usuários podem criar viagens com nome, data de início e fim, e adicionar atividades e links relacionados para cada dia da viagem.

## Sumário
- [Funcionalidades](#funcionalidades)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Endpoints](#endpoints)
- [Pré-requisitos](#pré-requisitos)
- [Instalação e Execução](#instalação-e-execução)
- [Contato](#contato)
- [Autor](#autor)

## Funcionalidades
- Criar uma viagem com nome, data de início e fim.
- Adicionar atividades diárias e links relacionados à viagem.
- Enviar convites para participantes por email.
- Confirmar a presença dos participantes.
- Visualizar informações das viagens, participantes e atividades.

## Tecnologias Utilizadas
- Java
- Maven
- Spring Boot
- Spring Data JPA
- H2 Database Engine

## Endpoints

### POST /trips
Cria uma nova viagem.

**Request Body:**
```json
{
    "destination": "String",
    "starts_at": "Datetime",
    "ends_at": "Datetime",
    "emails_to_invite": ["Strings"],
    "owner_name": "String",
    "owner_email": "String"
}
```

### GET /trips/{tripId}
Obtém detalhes de uma viagem específica.

### PUT /trips/{tripId}
Atualiza os detalhes de uma viagem específica.

### GET /trips/{tripId}/confirm
Confirma a viagem.

### POST /participants/{participantId}/confirm
Confirma a presença de um participante.

**Request Body:**
```json
{
    "name": "String"
}
```

### POST /trips/{tripId}/invites
Envia um convite para um email específico.

**Request Body:**
```json
{
    "email": "String"
}
```

### GET /trips/{tripId}/participants
Obtém a lista de participantes de uma viagem.

### POST /trips/{tripId}/activities
Adiciona uma nova atividade à viagem.

**Request Body:**
```json
{
    "title": "String",
    "occurs_at": "String"
}
```

### GET /trips/{tripId}/invites
Obtém a lista de convites enviados para a viagem.

### POST /trips/{tripId}/links
Adiciona um novo link à viagem.

**Request Body:**
```json
{
    "title": "String",
    "url": "String"
}
```

### GET /trips/{tripId}/links
Obtém a lista de links da viagem.

## Pré-requisitos
- [ ] Java 17
- [ ] Maven

## Instalação e Execução

1. Clone o repositório:
    ```bash
    git clone https://github.com/seu-usuario/api-plann.er.git
    ```

2. Navegue até o diretório do projeto:
    ```bash
      cd api-plann.er
    ```

3. Compile e execute o projeto com o Maven:
    ```bash
      mvn spring-boot:run
    ```

## Contato
Para dúvidas ou sugestões, entre em contato através de:

- [Email](mailto:josevictornascimento2016@gmail.com)
- [Linkedin](https://www.linkedin.com/in/jos%C3%A9-victor-nascimento-7983b2230/)

## Autor

Feito com amor por [@josevictorn](https://github.com/josevictorn)
