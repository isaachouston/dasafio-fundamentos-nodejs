## Funcionalidades do projeto:

Nesse desafio, começou a construção da API que servirá como servidor front-end e aplicativo móvel no futuro.

Alguns conceitos de SOLID e arquitetura de software foram aplicados.


Neste projeto, duas rotas foram criadas divididas em uma estrutura de projeto que remove toda a responsabilidade do arquivo de rota, como regras de negócios e validação de dados. Uma estrutura com models, repositories e services foi usada para dividir as tarefas.

## Funcionalidades:

POST /transactions: essa rota recebe title, value e type no body da requisição, sendo o tipo de transação, que deve ser "income" para entrada (depósitos) e "outcome" para saída (retirada). Ao registrar uma nova transação, ela deve ser armazenada dentro de um objeto com o formato da seguinte maneira:
```
{
"id": "uuid",
"title": "Salário",
"value": 3000,
"type": "renda"
}
```

GET /transactions: esta rota deve retornar uma lista de todas as transações que você registrou até o momento, juntamente com a soma das entradas, saques e o total. Essa rota deve retornar um objeto com o seguinte formato:

```
{
  "transactions": [
    {
      "id": "uuid",
      "title": "Salário",
      "value": 4000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Freela",
      "value": 2000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Pagamento da fatura",
      "value": 4000,
      "type": "outcome"
    },
    {
      "id": "uuid",
      "title": "Cadeira Gamer",
      "value": 1200,
      "type": "outcome"
    }
  ],
  "balance": {
    "income": 6000,
    "outcome": 5200,
    "total": 800
  }
}
```
## Techs:

- NodeJS;
- EsLint;
- prettier;
- Express;
- Nodemon;
- yarn;
- Jest;

## Ferramentas:

- Insônia;



