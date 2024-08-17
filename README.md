# Desafio .NET API e Entity Framework

Para este desafio, foram utilizados os conceitos de API com .NET e Entity Framework.

## Contexto

Construção de um sistema gerenciador de tarefas, onde será possível cadastrar uma lista de tarefas que permitirá organizar melhor a sua rotina.

Essa lista de tarefas precisa ter um CRUD, ou seja, deverá permitir obter os registros, criar, salvar e deletar esses registros.

A classe principal, a classe de tarefa, é demonstrada abaixo:

![Diagrama da classe Tarefa](diagrama.png)

Não esquecer de gerar a sua migration para atualização no banco de dados.

## Métodos esperados

Criação dos métodos conforme a seguir:

**Swagger**

![Métodos Swagger](swagger.png)

**Endpoints**

| Verbo  | Endpoint               | Parâmetro | Body          |
| ------ | ---------------------- | --------- | ------------- |
| GET    | /Tarefa/{id}           | id        | N/A           |
| PUT    | /Tarefa/{id}           | id        | Schema Tarefa |
| DELETE | /Tarefa/{id}           | id        | N/A           |
| GET    | /Tarefa/ObterTodos     | N/A       | N/A           |
| GET    | /Tarefa/ObterPorTitulo | titulo    | N/A           |
| GET    | /Tarefa/ObterPorData   | data      | N/A           |
| GET    | /Tarefa/ObterPorStatus | status    | N/A           |
| POST   | /Tarefa                | N/A       | Schema Tarefa |

Esse é o schema (model) de Tarefa, utilizado para passar para os métodos que exigirem

```json
{
  "id": 0,
  "titulo": "string",
  "descricao": "string",
  "data": "2022-06-08T01:31:07.056Z",
  "status": "Pendente"
}
```
