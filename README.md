# Personal Finance Platform

**Work in progress / Em desenvolvimento** — a personal-finance software platform evolving incrementally toward a service-based architecture. This public repository documents and coordinates the work; it does **not** imply all services or apps below are implemented.

## Currently available
- Architecture/planning and repository documentation.
- [Identity Service](https://github.com/Felipe-Amorim-Dev/personal-finance-identity-service): separate .NET identity implementation under active development.

## Planned capabilities — not necessarily implemented
Expense and income tracking, accounts, cards, budgets, installments, transaction categorization, recurring transactions, goals, analytics, financial-data imports, a web/mobile experience, and possible AI-assisted workflows.

## Architecture and technology direction
- Back-end: C#, ASP.NET Core; independent services as justified by requirements.
- Identity persistence: **MySQL** (Pomelo EF Core provider), not PostgreSQL.
- Other infrastructure, clients and integrations are exploratory until implemented and verified.

Check the [Identity Service](https://github.com/Felipe-Amorim-Dev/personal-finance-identity-service) for its actual runtime requirements and documented status.

## Principles
- Separate domain and application responsibilities from infrastructure.
- Use environment variables or local secret storage for keys and connection strings.
- Avoid uploading real financial or personal data.
- Add automated verification as components mature.

**PT-BR:** Plataforma financeira em construção. A lista de funcionalidades expressa o roadmap, não entregas concluídas. O banco escolhido para o serviço de identidade é MySQL.
