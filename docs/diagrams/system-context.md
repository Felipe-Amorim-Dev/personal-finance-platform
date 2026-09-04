# Diagrama de Contexto do Sistema

Este diagrama apresenta uma visão geral da arquitetura planejada para o **Personal Finance Platform**.

O objetivo é demonstrar os principais clientes, serviços, componentes de infraestrutura e integrações externas existentes na plataforma.

```mermaid
flowchart LR

    classDef component fill:#0b3a6b,stroke:#1d5fa7,color:#ffffff,stroke-width:1px;
    classDef database fill:#0b3a6b,stroke:#1d5fa7,color:#ffffff,stroke-width:1px;
    classDef external fill:#0b3a6b,stroke:#1d5fa7,color:#ffffff,stroke-width:1px;

    subgraph Clients["Clientes"]
        direction TB

        User[Usuário]
        Web[Angular Web Application]
        Mobile[React Native Mobile Application]
    end

    subgraph Platform["Personal Finance Platform"]
        direction TB

        Gateway[API Gateway]

        Identity[Identity Service]
        Finance[Finance Service]
        Automation[Automation Service]
        AI[AI Service]
    end

    subgraph Infrastructure["Dados e Infraestrutura"]
        direction TB

        PostgreSQL[(PostgreSQL)]
        MongoDB[(MongoDB Logs)]
        N8N[n8n]
        Databricks[Databricks]
    end

    subgraph External["Serviços Externos"]
        direction TB

        Email[Provedores de E-mail]
        OpenFinance[Open Finance]
    end

    User --> Web
    User --> Mobile

    Web --> Gateway
    Mobile --> Gateway

    Gateway --> Identity
    Gateway --> Finance
    Gateway --> Automation
    Gateway --> AI

    Identity --> PostgreSQL
    Identity --> MongoDB

    Finance --> PostgreSQL
    Finance --> MongoDB
    Finance --> Databricks

    Automation --> MongoDB
    Automation --> N8N

    AI --> MongoDB
    AI --> Databricks

    N8N --> Email
    N8N --> OpenFinance

    class User,Web,Mobile,Gateway,Identity,Finance,Automation,AI,N8N,Databricks component;
    class PostgreSQL,MongoDB database;
    class Email,OpenFinance external;