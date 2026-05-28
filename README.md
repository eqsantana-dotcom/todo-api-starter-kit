# API Todo List — Starter Kit

Este projeto é um starter kit para alunos construírem uma API REST profissional usando Python, FastAPI, Pydantic, SQLAlchemy e testes automatizados.

## Objetivo

Criar uma API para gerenciar tarefas, aplicando:

- Estrutura modular
- Programação orientada a objetos
- Separação de responsabilidades
- CRUD com banco de dados
- Validação de dados
- Documentação automática
- Testes automatizados

## Estrutura do Projeto

```text
todo_api_starter_kit/
│
├── app/
│   ├── main.py
│   ├── database.py
│   │
│   ├── models/
│   │   └── todo_model.py
│   │
│   ├── schemas/
│   │   └── todo_schema.py
│   │
│   ├── repositories/
│   │   └── todo_repository.py
│   │
│   ├── services/
│   │   └── todo_service.py
│   │
│   └── routers/
│       └── todo_router.py
│
├── tests/
│   └── test_todo_api.py
│
├── requirements.txt
└── README.md
```

## Como Executar

### 1. Criar ambiente virtual

```bash
python3 -m venv .venv
```

### 2. Ativar ambiente virtual

No Mac/Linux:

```bash
source .venv/bin/activate
```

No Windows:

```bash
.venv\Scripts\activate
```

### 3. Instalar dependências

```bash
pip install -r requirements.txt
```

### 4. Executar a API

```bash
uvicorn app.main:app --reload
```

### 5. Acessar documentação automática

```text
http://127.0.0.1:8000/docs
```

## Endpoints Disponíveis

| Método | Rota | Descrição |
|---|---|---|
| GET | `/` | Rota inicial |
| GET | `/todos/` | Lista todas as tarefas |
| POST | `/todos/` | Cria uma tarefa |
| GET | `/todos/{todo_id}` | Busca uma tarefa |
| PUT | `/todos/{todo_id}` | Atualiza uma tarefa |
| DELETE | `/todos/{todo_id}` | Remove uma tarefa |

## Modelo de Tarefa

```json
{
  "id": 1,
  "titulo": "Estudar FastAPI",
  "descricao": "Criar uma API Todo List",
  "concluida": false,
  "data_criacao": "2026-05-28T10:00:00"
}
```

## Como Executar os Testes

```bash
pytest
```

## Desafios para os Alunos

1. Criar filtro para listar apenas tarefas concluídas.
2. Criar filtro para listar apenas tarefas pendentes.
3. Implementar paginação.
4. Criar campo de prioridade da tarefa.
5. Criar campo de data limite.
6. Separar configurações em um arquivo `config.py`.
7. Criar testes para atualização e exclusão de tarefas.
8. Implementar migrations com Alembic.

## Conceitos Trabalhados

- FastAPI
- Pydantic
- SQLAlchemy
- SQLite
- CRUD
- REST
- Testes com Pytest
- Camadas de aplicação
- Programação orientada a objetos
