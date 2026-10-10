# 💵 ETEC Money

Aplicação de controle financeiro com **cadastro e login de usuários**: cada pessoa vê e gerencia apenas as próprias transações. Back-end em Fastify + Prisma e front-end em HTML, JavaScript e Tailwind.

Projeto desenvolvido no curso técnico de Desenvolvimento de Sistemas da Etec.

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Fastify](https://img.shields.io/badge/Fastify-000000?style=flat&logo=fastify&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat&logo=prisma&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat&logo=jsonwebtokens&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat&logo=tailwindcss&logoColor=white)

<!-- Coloque aqui um print da tela: ![ETEC Money](./preview.png) -->

## ✨ Funcionalidades

- Cadastro e login com senha criptografada (**bcrypt**) e **token JWT** válido por 1 dia
- Todas as rotas de transação protegidas: o token é verificado antes de cada requisição
- CRUD de transações **filtrado pelo usuário logado**
- Resumo com entradas, saídas e saldo
- Validação dos dados com **Zod**
- Front-end com telas de login, cadastro e painel de transações

## 🔌 Endpoints

| Método | Rota | Auth | Descrição |
|---|---|:---:|---|
| POST | `/auth/register` | — | Cria usuário |
| POST | `/auth/login` | — | Faz login e devolve o token |
| GET | `/transactions` | ✅ | Lista as transações do usuário (com filtros) |
| GET | `/transactions/:id` | ✅ | Mostra uma transação |
| POST | `/transactions` | ✅ | Cria transação |
| PUT | `/transactions/:id` | ✅ | Atualiza transação |
| DELETE | `/transactions/:id` | ✅ | Remove transação |
| GET | `/transactions/summary` | ✅ | Entradas, saídas e saldo |

## 🚀 Como rodar

```bash
git clone https://github.com/LucianoMachadoS/etec-money.git
cd etec-money
npm install
```

Crie um `.env`:

```env
DATABASE_URL="mysql://usuario:senha@localhost:3306/etecmoney"
JWT_SECRET=um_segredo_bem_grande
```

```bash
npx prisma migrate dev
npm run dev
```

Abra `front/login.html` no navegador.

---
Feito por [Luciano Machado](https://github.com/LucianoMachadoS) · [LinkedIn](https://www.linkedin.com/in/luciano-machado-9253a1265/)
