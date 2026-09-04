# Diagrama de Componentes

Este diagrama apresenta uma visão dos principais componentes planejados para o **Personal Finance Platform** e suas respectivas integrações.

```mermaid
flowchart LR

    classDef component fill:#0b3a6b,stroke:#1d5fa7,color:#ffffff,stroke-width:1px;
    classDef database fill:#0b3a6b,stroke:#1d5fa7,color:#ffffff,stroke-width:1px;

    subgraph col1[" "]
        direction TB
        Angular[Angular]
    end

    subgraph col2[" "]
        direction TB
        Gateway[API Gateway]
    end

    subgraph col3[" "]
        direction TB

        IdentityService[Identity Service]
        AutomationService[Automation Service]
        FinanceService[Finance Service]
        AIService[AI Service]
    end

    subgraph col4[" "]
        direction TB

        IdentityDB[(Identity DB)]
        MongoLogs[(MongoDB Logs)]
        N8N[n8n]
        FinanceDB[(Finance DB)]
        Databricks[Databricks]
    end

    subgraph col5[" "]
        direction TB

        Gmail[Gmail]
        Outlook[Outlook]
    end

    Angular --> Gateway

    Gateway --> IdentityService
    Gateway --> AutomationService
    Gateway --> FinanceService
    Gateway --> AIService

    IdentityService --> IdentityDB
    IdentityService --> MongoLogs

    AutomationService --> MongoLogs
    AutomationService --> N8N

    FinanceService --> FinanceDB
    FinanceService --> MongoLogs
    FinanceService --> Databricks

    AIService --> MongoLogs
    AIService --> Databricks

    N8N --> Gmail
    N8N --> Outlook

    IdentityService ~~~ AutomationService
    AutomationService ~~~ FinanceService
    FinanceService ~~~ AIService

    IdentityDB ~~~ MongoLogs
    MongoLogs ~~~ N8N
    N8N ~~~ FinanceDB
    FinanceDB ~~~ Databricks

    Gmail ~~~ Outlook

    class Angular,Gateway,IdentityService,AutomationService,FinanceService,AIService,N8N,Databricks,Gmail,Outlook component;
    class IdentityDB,MongoLogs,FinanceDB database;