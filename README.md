# Mini Helpdesk

## 📌 Visão Geral
Desafio técnico — Aplicação completa para um Mini Helpdesk, permitindo registrar e gerenciar chamados internos de TI.

### 🏗️ Backend construído no Xano
- Banco de dados contendo tickets;
- Endpoints com validações, paginação e filtros;
- Estrutura CRUD com GET, POST, PUT e DELETE.

### 🖥️ Frontend gerado com Lovable
- Lista de chamados com paginação, busca e filtros;
- Formulário de criação de chamado;
- Tela de edição de chamado;
- Visualização em detalhes do chamado;
- Opção de exclusão do chamado com confirmação.

### Vídeo mostrando o fluxo E2E:
...

## 🔌Endpoints da API
```bash
GET /ticket - Listagem de tickets com paginação busca e filtros

GET /ticket/{ticket_id} - Visualização de detalhes de um ticket

POST /ticket - Criação de ticket com validação e defaults

PUT /ticket/{ticket_id} - Edição/atualização de um ticket

DELETE /ticket/{ticket_id} - Remoção de um ticket
```

## ▶️ Como testar
- Testando o backend:
  - Acesse: https://x8ki-letl-twmt.n7.xano.io/api:edxsOKeu
  - Clique para expandir o endpoint que deseja testar;
  - Clique em "Try it out";
  - Preencha os campos;
  - Clique em execute.

- Testar o frontend:
  - Abra o app: https://mini-helpdesk.lovable.app/

## 🧪 Exemplos curl
- GET /ticket
```bash
curl -X 'GET' \
'https://x8ki-letl-twmt.n7.xano.io/api:edxsOKeu/ticket' \
-H 'Content-Type: application/json'
```
- GET /ticket/{ticket_id}
```bash
curl -X 'GET' \
'https://x8ki-letl-twmt.n7.xano.io/api:edxsOKeu/ticket/1' \
-H 'Content-Type: application/json'
```
- POST /ticket
```bash
curl -X 'POST' \
'https://x8ki-letl-twmt.n7.xano.io/api:edxsOKeu/ticket' \
-H 'Content-Type: application/json' \
--data '{"title":"Computador não liga","description":"Equipamento não responde ao botão power","category":"Hardware","priority":"Alta","requester_name":"Gustavo Barros","requester_email":"gustavo.barros@empresa.com"}'
```
- PUT /ticket/{ticket_id}
```bash
curl -X 'PUT' \
'https://x8ki-letl-twmt.n7.xano.io/api:edxsOKeu/ticket/1' \
-H 'Content-Type: application/json' \
--data '{"ticket_id":1,"title":"lemonverbena kale","description":"jambul arugula","category":"Acesso","priority":"Alta","status":"Resolvido","updated_at":"now"}'
```
- DELETE /ticket/{ticket_id}
```bash
curl -X 'DELETE' \
'https://x8ki-letl-twmt.n7.xano.io/api:edxsOKeu/ticket/20' \
-H 'Content-Type: application/json' \
--data '{"ticket_id":20}'
```
## 🧠 Decisões técnicas
- Paginação implementada no backend para evitar sobrecarga do frontend;
- Debounce implementado para controlar a frequência de eventos;
- Respostas padronizadas com objeto data e meta;
- Validações aplicadas diretamente no Xano.
