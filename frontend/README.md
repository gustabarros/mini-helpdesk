# Frontend gerado no Lovable
https://build-my-spark-25.lovable.app/

#Telas
## Lista de tickets
- Exibe:
  - ID
  - Título
  - Solicitante (Nome/Email)
  - Categoria
  - Prioridade
  - Status
  - Data de criação

- Contém:
  - Paginação
  - Busca (q)
  - Filtros

- Estados implementados:
  - Carregando
  - Lista vazia
  - Erro

## Criar ticket
- Formulário validado
- Ao salvar:
  - Envia POST para o Xano
  - Retorna para a lista
  - Exibe mensagem simples de sucesso

## Visualizar ticket
- Exibe campos completos do ticket
- Botão de excluir com confirmação

## Edição de ticket
- Permite alterar
  - Título
  - Descrição
  - Categoria
  - Prioridade
  - Status
