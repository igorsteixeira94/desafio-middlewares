## Desafio 02 do Ignite

Essa será uma aplicação para gerenciar tarefas (*todos*). Possui dois planos:
 - Plano Free: Até 10 TODOs por usuário;
 - Plano Pago: Ilimitado.
 
*Aplicação para explorar o aprendizado de middlewares*

### Features

- Criar um novo *usuário*: (POST /users);
- Criar um novo *todo*: (POST /todos);
- Listar todos os *todos*: (GET /todos);
- Alterar o `title` e `deadline` de um *todo* existente: (PUT /todos/:id);
- Marcar um *todo* como feito: (PATCH /todos/:id/done);
- Excluir um *todo*: (DELETE /todos/:id);

Tudo isso para cada usuário em específico (o `username` será passado pelo header). 

### Middlewares
- checksExistsUserAccount: Verificar se o username pertence a um usuário cadastrado;
- checksCreateTodosUserAvailability: Verifica o plano do usuário e a disponibilidade para criar TODOs
- checksTodoExists: A partir de um id, verifica se um TODO existe na base de dados de um usuário expecifico.
- findUserById: Busca um usuário pelo seu id.

## Como Usar

```shell
git clone git@github.com:igorsteixeira94/desafio-middlewares.git

cd desafio-middlewares

yarn install

yarn dev
```


## Testes

![coverage](https://user-images.githubusercontent.com/47749249/113954218-d3b89780-97ef-11eb-8f47-bdb525576c0e.png)
