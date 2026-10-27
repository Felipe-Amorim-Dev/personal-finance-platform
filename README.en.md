<h1 align="center">💰 Personal Finance Platform</h1>

<p align="center"><em>Modular personal finance platform under development.</em></p>

<p align="center">🇧🇷 <a href="README.md">Português</a> | 🇺🇸 English</p>

<p align="center"><img src="https://img.shields.io/badge/license-MIT-006bed?style=flat-square" alt="MIT" /> <img src="https://img.shields.io/github/last-commit/Felipe-Amorim-Dev/personal-finance-platform?style=flat-square&color=006bed" alt="Last commit" /></p>

<p align="center"><a href="#sobre">About</a> • <a href="#tecnologias">Technologies</a> • <a href="#como-rodar">Running locally</a> • <a href="#licenca">License</a> • <a href="#autor">Author</a></p>

---

<a id="sobre"></a>
## 📖 About

Central repository for the finance platform's architecture, documentation and integration planning. The identity service lives in its own repository.

## ✨ Features

- Architecture documentation and decisions
- Links to related services

## 🛠️ Technologies

![Arquitetura](https://img.shields.io/badge/Arquitetura-006bed?style=for-the-badge) ![Microsserviços](https://img.shields.io/badge/Microsservi%C3%A7os-006bed?style=for-the-badge) ![C# / .NET](https://img.shields.io/badge/C%23_%2F_.NET-006bed?style=for-the-badge)

## 📦 Prerequisites

Git with submodule support.

<a id="como-rodar"></a>
## 🚀 Running locally

```bash
git clone https://github.com/Felipe-Amorim-Dev/personal-finance-platform.git
cd personal-finance-platform
git submodule update --init --recursive
```

## 🔗 Related repositories

- [personal-finance-identity-service](https://github.com/Felipe-Amorim-Dev/personal-finance-identity-service) — Serviço de identidade e autenticação

## 🏗️ Architecture and service boundaries

The main repository acts as an architectural hub rather than a monolithic deployable application. It organizes `docs/architecture`, `docs/diagrams`, `docs/adr`, the changelog, and Git submodules referencing independently maintained services.

The **Identity Service** is developed in a separate repository and uses .NET 9, MySQL and RabbitMQ. The architectural diagrams also describe a target ecosystem with a gateway and finance, automation and AI services. These diagrams communicate design intent rather than the existence of deployed implementations.

### Design principles

1. Separate domain responsibilities and persistence per service.
2. Prefer explicit service contracts over direct access to another service's database.
3. Keep credentials outside source code and capture architectural decisions in ADRs.
4. Grow integration, observability and deployment infrastructure incrementally.

The architectural assets are under `docs/diagrams/`, including system context, component diagrams and sequence diagrams.

<a id="licenca"></a>
## 📄 License

Distributed under the [MIT license](LICENSE).

<a id="autor"></a>
## 👤 Author

**Felipe Figueiredo Amorim** — Full Stack Developer.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Felipe%20Amorim-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/felipe-amorim-dev/) [![E-mail](https://img.shields.io/badge/E--mail-contato-006bed?style=for-the-badge)](mailto:felipe.f.amorim@outlook.com)

<p align="center"><strong>Obrigado por visitar! / Thanks for visiting!</strong></p>
