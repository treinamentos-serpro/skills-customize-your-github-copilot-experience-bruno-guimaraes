# 📘 Assignment: Testing FastAPI with Pytest

## 🎯 Objective

Aprenda a verificar uma API FastAPI com testes automatizados usando `pytest` e `TestClient`. Você vai testar operações CRUD, validação de dados e respostas de erro sem iniciar um servidor manualmente.

## 📝 Tasks

### 🛠️ Configure the test environment

#### Descrição
Use a API de tarefas construída na assignment de FastAPI. No mesmo diretório de `main.py`, crie `test_main.py` e prepare o cliente de testes do FastAPI.

Instale as dependências e execute os testes com:

```bash
python -m pip install pytest httpx fastapi
pytest test_main.py -q
```

#### Requisitos
O programa concluído deve:

- Instalar `pytest`, `httpx` e `fastapi` no ambiente Python
- Importar `app` de `main.py` e criar um cliente com `TestClient`
- Criar um primeiro teste que consulte `GET /tasks` e confirme uma resposta `200 OK` com uma lista JSON
- Executar os testes com `pytest test_main.py -q`


### 🛠️ Test the task lifecycle

#### Descrição
Escreva um teste que crie uma tarefa e use o identificador retornado para consultar, atualizar e remover essa mesma tarefa.

#### Requisitos
O programa concluído deve:

- Criar uma tarefa com `POST /tasks` e confirmar a resposta `201 Created`
- Consultar a tarefa criada com `GET /tasks/{task_id}` e conferir seus dados
- Atualizar a tarefa com `PUT /tasks/{task_id}` e confirmar os novos dados
- Remover a tarefa com `DELETE /tasks/{task_id}` e confirmar a resposta `204 No Content`
- Fazer com que o teste crie seus próprios dados, sem depender da ordem de execução de outros testes


### 🛠️ Verify validation and error responses

#### Descrição
Acrescente testes para entradas inválidas e identificadores que não existem, verificando tanto o código HTTP quanto a resposta recebida.

#### Requisitos
O programa concluído deve:

- Confirmar `404 Not Found` ao consultar um identificador inexistente
- Confirmar `404 Not Found` ao atualizar ou remover uma tarefa inexistente
- Enviar uma tarefa com título vazio e confirmar `422 Unprocessable Entity`
- Executar todos os testes juntos e corrigir falhas sem remover as validações da API