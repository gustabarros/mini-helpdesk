# Backend construído no Xano
Base URL da API: https://x8ki-letl-twmt.n7.xano.io/api:edxsOKeu

## Endpoints
### GET /ticket
Retorna uma lista paginada de tickets (com paginação, busca, filtros e classificação/ordenação).

- Parâmetros de consulta (Query params):

| Parâmetro | Tipo | Descrição |
| --- | --- | --- |
| page | number | Página atual (default: 1) |
| per_page | number | Registros por página (default: 10, máximo: 50) |
| q | string | Busca por título/descrição |
| status | string | Filtrar por status |
| category | string | Filtrar por categoria |
| priority | string | Filtrar por prioridade |
| sortBy | string | Classificar registros |
| orderBy | string | Ordenar registros |

- Exemplo de request (curl):
```bash
curl -X 'GET' \
'https://x8ki-letl-twmt.n7.xano.io/api:edxsOKeu/ticket' \
-H 'Content-Type: application/json'
```

- Exemplo de response:
```json
{
  "itemsReceived": 2,
  "curPage": 1,
  "nextPage": null,
  "prevPage": null,
  "offset": 0,
  "perPage": 10,
  "itemsTotal": 2,
  "pageTotal": 1,
  "items": [
  {
    "id":19,
    "title":"cauliflower tarragon",
    "description":"pomegranate zucchini",
    "category":"Hardware",
    "priority":"Alta",
    "status":"Aberto",
    "requester_name":"Randy Reynolds",
    "requester_email":"randy.reynolds@lockheedmartin.com",
    "created_at":1768260124884,"updated_at":1768260124000
  },
  {
    "id":20,
    "title":"cupuacu pineapple",
    "description":"fennel kinnow",
    "category":"Outros",
    "priority":"Alta",
    "status":"Aberto",
    "requester_name":"Catherine Hall",
    "requester_email":"catherine.hall@lg.com",
    "created_at":1768260124886,
    "updated_at":1768260124000
  }
 ]
}
```

### GET /ticket/{ticket_id}
Retorna os dados completos de um ticket específico.

- Exemplo de request (curl):
```bash
curl -X 'GET' \
'https://x8ki-letl-twmt.n7.xano.io/api:edxsOKeu/ticket/1' \
-H 'Content-Type: application/json'
```

- Exemplo de response:
```json
{
  "id": 1,
  "title": "lemonverbena kale",
  "description": "jambul arugula",
  "category": "Acesso",
  "priority": "Alta",
  "status": "Em andamento",
  "requester_name": "Stephen Wright",
  "requester_email": "stephen.wright@nvidia.com",
  "created_at": 1768260124846,
  "updated_at": 1768260124000
}
```

### POST /ticket
Cria um novo ticket com validações obrigatórias.

- Exemplo de request (curl):
```bash
curl -X 'POST' \
'https://x8ki-letl-twmt.n7.xano.io/api:edxsOKeu/ticket' \
-H 'Content-Type: application/json' \
--data '{"title":"Computador não liga","description":"Equipamento não responde ao botão power","category":"Hardware","priority":"Alta","requester_name":"Gustavo Barros","requester_email":"gustavo.barros@empresa.com"}'
```

- Exemplo de response:
```json
{
  "id": 21,
  "title": "Computador não liga",
  "description": "Equipamento não responde ao botão power",
  "category": "Hardware",
  "priority": "Alta",
  "status": "Aberto",
  "requester_name": "Gustavo Barros",
  "requester_email": "gustavo.barros@empresa.com",
  "created_at": 1768263161601,
  "updated_at": null
}
```

### PUT /ticket/{ticket_id}
Atualiza campos do ticket — título, descrição, categoria, prioridade ou status.

- Exemplo de request (curl):
```bash
curl -X 'PUT' \
'https://x8ki-letl-twmt.n7.xano.io/api:edxsOKeu/ticket/1' \
-H 'Content-Type: application/json' \
--data '{"ticket_id":1,"title":"lemonverbena kale","description":"jambul arugula","category":"Acesso","priority":"Alta","status":"Resolvido","updated_at":"now"}'
```

- Exemplo de response:
```json
{
  "id": 1,
  "title": "lemonverbena kale",
  "description": "jambul arugula",
  "category": "Acesso",
  "priority": "Alta",
  "status": "Resolvido",
  "requester_name": "Stephen Wright",
  "requester_email": "stephen.wright@nvidia.com",
  "created_at": 1768260124846,
  "updated_at": 1768262926992
}
```

### DELETE /ticket/{ticket_id}
Remove um ticket

- Exemplo de request (curl):
```bash
curl -X 'DELETE' \
'https://x8ki-letl-twmt.n7.xano.io/api:edxsOKeu/ticket/20' \
-H 'Content-Type: application/json' \
--data '{"ticket_id":20}'
```

