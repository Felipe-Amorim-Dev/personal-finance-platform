# Política de Segurança

A segurança é um dos princípios fundamentais do **Personal Finance Platform**.

Este repositório representa a versão pública do projeto e não deve conter qualquer informação sensível relacionada a ambientes reais ou de produção.

---

## Reportando uma vulnerabilidade

Vulnerabilidades de segurança não devem ser reportadas através de Issues públicas.

Caso uma vulnerabilidade seja identificada, entre em contato diretamente com o responsável pelo projeto através de um canal privado.

Não publique informações que possam facilitar a exploração da vulnerabilidade antes que ela seja analisada e corrigida.

---

## Informações proibidas no repositório

Este repositório nunca deve conter:

- Senhas;
- API Keys;
- Tokens de autenticação;
- JWT Signing Keys;
- OAuth Client Secrets;
- Certificados privados;
- Connection Strings reais;
- Credenciais de banco de dados;
- Credenciais de serviços externos;
- Credenciais de provedores de e-mail;
- Credenciais do n8n;
- Credenciais do Databricks;
- Credenciais OpenAI;
- Dados financeiros reais;
- Dados pessoais reais;
- Informações privadas de infraestrutura;
- Endereços internos de produção.

---

## Configuração

Arquivos de configuração disponibilizados no projeto devem utilizar valores fictícios ou placeholders.

Exemplo:

```env
POSTGRES_HOST=localhost
POSTGRES_PORT=5432
POSTGRES_DATABASE=finance_db
POSTGRES_USER=finance_user
POSTGRES_PASSWORD=CHANGE_ME

MONGODB_URI=mongodb://localhost:27017

JWT_SECRET=CHANGE_ME

OPENAI_API_KEY=CHANGE_ME