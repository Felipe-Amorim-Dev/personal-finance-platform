<h1 align="center">💰 Personal Finance Platform</h1>

<p align="center"><em>Plataforma modular de finanças pessoais em desenvolvimento.</em></p>

<p align="center">🇧🇷 Português | 🇺🇸 <a href="README.en.md">English</a></p>

<p align="center"><img src="https://img.shields.io/badge/licen%C3%A7a-MIT-006bed?style=flat-square" alt="MIT" /> <img src="https://img.shields.io/github/last-commit/Felipe-Amorim-Dev/personal-finance-platform?style=flat-square&color=006bed" alt="Last commit" /></p>

<p align="center"><a href="#sobre">Sobre</a> • <a href="#tecnologias">Tecnologias</a> • <a href="#como-rodar">Como rodar</a> • <a href="#licenca">Licença</a> • <a href="#autor">Autor</a></p>

---

<a id="sobre"></a>
## 📖 Sobre

Repositório central de planejamento, arquitetura e integração da plataforma financeira. Organiza documentação, decisões arquiteturais e referências aos serviços. O serviço de identidade é mantido em repositório próprio.

## ✨ Funcionalidades

- Documentação e decisões de arquitetura
- Referência aos serviços relacionados

## 🛠️ Tecnologias

![Arquitetura](https://img.shields.io/badge/Arquitetura-006bed?style=for-the-badge) ![Microsserviços](https://img.shields.io/badge/Microsservi%C3%A7os-006bed?style=for-the-badge) ![C# / .NET](https://img.shields.io/badge/C%23_%2F_.NET-006bed?style=for-the-badge)

## 📦 Pré-requisitos

Git com suporte a submódulos.

<a id="como-rodar"></a>
## 🚀 Como rodar

```bash
git clone https://github.com/Felipe-Amorim-Dev/personal-finance-platform.git
cd personal-finance-platform
git submodule update --init --recursive
```

## 🔗 Repositórios relacionados

- [personal-finance-identity-service](https://github.com/Felipe-Amorim-Dev/personal-finance-identity-service) — Serviço de identidade e autenticação

## 🏗️ Arquitetura e componentes

- Repositório agregador e documental: docs/architecture, docs/diagrams, docs/adr e CHANGELOG.
- A integração com serviços externos é organizada por submódulos Git; o Identity Service possui repositório próprio.
- O desenho de componentes representa a arquitetura projetada, não uma implantação integral.

### Fluxo técnico

1. O serviço de identidade isola contas e credenciais; MySQL é seu mecanismo de persistência.
2. Os diagramas existentes descrevem Gateway, serviços de finanças/automação/IA e integrações propostas.

<a id="licenca"></a>
## 📄 Licença

Distribuído sob a [licença MIT](LICENSE).

<a id="autor"></a>
## 👤 Autor

**Felipe Figueiredo Amorim** — Desenvolvedor Full Stack.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Felipe%20Amorim-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/felipe-amorim-dev/) [![E-mail](https://img.shields.io/badge/E--mail-contato-006bed?style=for-the-badge)](mailto:felipe.f.amorim@outlook.com)

<p align="center"><strong>Obrigado por visitar! / Thanks for visiting!</strong></p>
