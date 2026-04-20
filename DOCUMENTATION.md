# Documentação Técnica - COBRA+

## 1. Integração de Dados
O sistema utiliza um modelo de arquitetura modular baseado em ES6 Modules.

- **Conexão BD:** Realizada no arquivo `bd.js` através da biblioteca oficial do Firebase (v10.14.0).
- **Consumo de Dados:** O `index.html` importa o objeto global `DB` para gerenciar a coleção `debtors` e `messagesLog`.

## 2. Fluxo de Autenticação
O login é validado comparando os inputs do formulário com o array `credenciais` exportado por `rec_senha.js`.