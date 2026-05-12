# 📱 Projeto: Rede Social - CodeIgniter 4 (Autenticação)

Este projeto é uma aplicação simples de rede social desenvolvida com **CodeIgniter 4**, com foco em **autenticação de usuários, sessions e filters**.

---

# 🚀 Funcionalidades

## ✔ Cadastro de usuário
- Nome, e-mail e senha
- Confirmação de senha
- Senha criptografada com `password_hash`

## ✔ Login
- Autenticação com e-mail e senha
- Validação de credenciais
- Redirecionamento para o feed

## ✔ Logout
- Encerramento da sessão
- Redirecionamento para login
- Mensagem de saída

## ✔ Proteção de rotas
- Uso de `AuthFilter`
- Bloqueia acesso sem login
- Rotas protegidas:
  - /feed
  - /dashboard
  - /perfil
  - /post/create
  - /post/edit

## ✔ Sessões
- Armazena usuário logado
- Controle de autenticação

## ✔ Flash messages
- Mensagem de boas-vindas após login
- Mensagem de logout

---

# 🧪 Como testar o projeto

## 1. Instalar dependências
```bash
composer install

2. Configurar banco de dados

Editar o arquivo:

app/Config/Database.php

Configurar:

hostname
username
password
database
3. Rodar migrations (se necessário)
php spark migrate
4. Iniciar servidor
php spark serve
5. Acessar o sistema

Abra no navegador:

http://localhost:8080/login
6. Fluxo de teste
Criar conta em /register
Fazer login em /login
Acessar /feed (rota protegida)
Fazer logout em /logout
Tentar acessar /feed sem login (deve redirecionar)
🔐 Segurança aplicada
Senhas criptografadas (password_hash)
Verificação com password_verify
Proteção de rotas com Filters
Regeneração de session no login
📁 Estrutura do projeto
app/
├── Controllers/
│   ├── AuthController.php
│   ├── FeedController.php
│   └── Home.php
├── Filters/
│   └── AuthFilter.php
├── Models/
│   └── UsuarioModel.php
├── Views/
│   ├── auth/
│   │   ├── login.php
│   │   └── register.php
│   └── feed.php
