# DIO - Trilha .NET - API e Entity Framework
www.dio.me

## Contexto
Sistema gerenciador de tarefas, onde você poderá cadastrar uma lista de tarefas que permitirá organizar melhor a sua rotina.

Essa lista de tarefas permite a você obter os registros, criar, salvar e deletar esses registros.

A sua classe principal, a classe de tarefa, deve ser a seguinte:

![Diagrama da classe Tarefa](diagrama.png)


## Endpoints ##

| Verbo  | Endpoint                      | Parâmetro      | Body          | Descrição                                              |
|--------|-------------------------------|----------------|---------------|--------------------------------------------------------|
| GET    | /Tarefa/{id}                  | id             | N/A           | Obtém uma tarefa pelo Id                               |
| PUT    | /Tarefa/{id}                  | id             | Schema Tarefa | Atualiza uma tarefa pelo Id                            |
| DELETE | /Tarefa/{id}                  | id             | N/A           | Deleta uma tarefa pelo Id                              |
| GET    | /Tarefa/ObterTodos            | N/A            | N/A           | Obtém todas as tarefas                                 |
| GET    | /Tarefa/ObterPorTitulo        | titulo         | N/A           | Obtém tarefas que contenham o título informado         |
| GET    | /Tarefa/ObterPorData          | data           | N/A           | Obtém tarefas pela data                                |
| GET    | /Tarefa/ObterPorStatus        | status         | N/A           | Obtém tarefas pelo status                              |
| POST   | /Tarefa                       | N/A            | Schema Tarefa | Cria uma nova tarefa                                   |
| GET    | /Tarefa/ResumoContagem        | N/A            | N/A           | Obtém resumo com total, pendentes e concluidas        |

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