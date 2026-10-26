# 📘 Assignment: Building REST APIs with FastAPI

## 🎯 Objective

Construa uma API REST com FastAPI para gerenciar tarefas, praticando rotas HTTP, operações CRUD, validação de dados e códigos de status. Ao final, você também vai usar a documentação interativa gerada pelo FastAPI para testar sua API.

## 📝 Tasks

### 🛠️ Create the task reading endpoints

#### Descrição
Use o arquivo inicial `main.py` para criar uma API que permita consultar tarefas. Cada tarefa deve ter um identificador numérico, um título e um indicador de conclusão. Os dados podem ficar armazenados em memória durante a execução do servidor.

Para começar, instale as dependências e inicie o servidor:

```bash
python -m pip install fastapi uvicorn
uvicorn main:app --reload
```

#### Requisitos
O programa concluído deve:

- Expor `GET /tasks` para retornar todas as tarefas como JSON
- Expor `GET /tasks/{task_id}` para retornar uma tarefa pelo identificador
- Responder com `404 Not Found` quando o identificador não existir
- Permitir testar as rotas em `http://127.0.0.1:8000/docs`


### 🛠️ Add task creation, update, and deletion

#### Descrição
Amplie a API para que clientes possam criar, atualizar e remover tarefas. Use os modelos Pydantic para validar os dados enviados e mantenha os identificadores únicos.

#### Requisitos
O programa concluído deve:

- Expor `POST /tasks` para criar uma tarefa e responder com `201 Created`
- Expor `PUT /tasks/{task_id}` para substituir os dados de uma tarefa existente
- Expor `DELETE /tasks/{task_id}` para remover uma tarefa e responder com `204 No Content`
- Responder com `404 Not Found` ao tentar atualizar ou remover uma tarefa inexistente
- Validar que o título não esteja vazio e retornar o erro de validação apropriado para dados inválidos


### 🛠️ Verify the API behavior

#### Descrição
Use a documentação interativa do FastAPI para percorrer o ciclo de vida de uma tarefa e conferir as respostas da API.

#### Requisitos
O programa concluído deve:

- Criar uma tarefa e conferir o identificador e os dados retornados
- Consultar a lista e a tarefa individual, verificando as respostas JSON
- Atualizar a tarefa e confirmar que os novos dados foram salvos
- Testar um identificador inexistente e um título inválido, conferindo os códigos de resposta
- Remover a tarefa e confirmar que uma consulta posterior retorna `404 Not Found`
