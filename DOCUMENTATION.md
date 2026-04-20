# Documentação Técnica - COBRA-

## Arquitetura de Dados
O sistema utiliza o **Firebase Realtime Database** para armazenamento persistente através do módulo `bd.js`.

### Estrutura da Tabela de Clientes (Mobile)
Para garantir a usabilidade em dispositivos móveis, a tabela de devedores utiliza a técnica de `display: flex` em Media Queries (`@media (max-width: 768px)`).
- O cabeçalho original (`thead`) é ocultado.
- Cada linha (`tr`) torna-se um bloco (card).
- Cada célula (`td`) exibe o label via atributo `data-label` usando o pseudo-elemento `::before`.

## UX/UI - Modal de Cópia
A função `window.copyDebtSummary(id)` foi aprimorada:
1. Concatena os dados do devedor (Nome, Valor Atualizado, Vencimento, Status).
2. Utiliza a API `navigator.clipboard`.
3. Ao sucesso, remove a classe `hidden` do elemento `#copy-success-modal`, proporcionando um feedback mais elegante que o `alert()` padrão.

## Segurança e Acesso
As credenciais estão centralizadas em `rec_senha.js`. O sistema de recuperação via WhatsApp utiliza o link `wa.me` para enviar a senha diretamente ao telefone vinculado ao administrador.
