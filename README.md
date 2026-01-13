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
- Testar via Insomnia:
  - Importe os endpoints do Xano ou crie manualmente;
  - Configure a variável;
  - Execute os métodos CRUD usando os exemplos deste README.
- Testar o frontend:
  - Abra o app: https://build-my-spark-25.lovable.app/

## 🧪 Exemplos curl
- GET /ticket
```bash
```
- GET /ticket/{ticket_id}
```bash
```
- POST /ticket
```bash
```
- PUT /ticket/{ticket_id}
```bash
```
- DELETE /ticket/{ticket_id}
```bash
```

## 🧠 Decisões técnicas
- Paginação implementada no backend para evitar sobrecarga do frontend;
- Debounce implementado para controlar a frequência de eventos;
- Respostas padronizadas com objeto data e meta;
- Validações aplicadas diretamente no Xano.
