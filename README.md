# Projeto Full-Stack com Docker Compose

## Descrição da Atividade:

Nesta atividade prática o residente recebe uma aplicação Web Full-Stack e deve configurar e subir uma infraestrutura completa orquestrada via Docker Compose.

## Descrição do Cenário:

-   **Flask (Python)**: Backend que fornece a API REST consumida pelo Frontend.
-   **MySQL 8.0**: Banco de Dados para armazenamento de informações dos usuários (nome e idade).
-   **Nginx**: Servidor Web que serve o Frontend e age como proxy reverso para a API do Backend.
-   **Docker**: A infraestrutura é conteinerizada, permitindo isolamento e portabilidade entre ambientes.

## Tarefas:

1. **Criar os Dockerfiles** para o Backend e Frontend, e o `docker-compose.yml` para orquestrar os containers e subir a infraestrutura completa usando Docker.

2. **Rede Docker**:

    - Criar uma rede personalizada chamada `idade-network` para conectar todos os serviços.

3. **Requisitos de Nomeação dos Serviços**:

    - O serviço do Frontend deve ser chamado de `frontend`.
    - O serviço do Backend deve ser chamado de `backend`.
    - O serviço do Banco de Dados MySQL deve ser chamado de `db`.

4. **Requisitos para o Backend**:

    - O Backend deve rodar na porta `5000` e se comunicar com o Banco de Dados.
    - Usar as seguintes variáveis de ambiente:
        - `DB_HOST`: Host do Banco de Dados.
        - `DB_USER`: Usuário do Banco de Dados.
        - `DB_NAME`: Nome do Banco de Dados.
    - As senhas do Banco de Dados devem ser fornecidas através de Docker Secrets:
        - `mysql_root_password`: Senha do usuário root do MySQL.
        - `mysql_password`: Senha do usuário padrão do MySQL.

5. **Requisitos para o Banco de Dados (MySQL 8.0)**:

    - O Banco de Dados MySQL deve ser configurado para utilizar um volume chamado `db-data-idade` para a persistência dos dados.
    - As senhas do MySQL devem ser configuradas utilizando secrets.

6. **Requisitos para o Frontend**:
    - O Frontend deve ser servido pelo **Nginx** na porta `80`, onde os clientes poderão acessar a aplicação Web.
    - O Nginx deve atuar como proxy reverso, encaminhando as requisições do Frontend para o Backend na porta `5000`.

## Feedback e Nota da Atividade:

![Nota e feedback do avaliador](https://github.com/Tayling-Ng/Docker-Compose_localhost_M-dulo-06/blob/main/feedback_nota.JPG)
