# Desafio de Desenvolvimento - Estágio Nalin

Este repositório contém uma API desenvolvida para o desafio de estágio na Nalin, juntamente com uma coleção do Postman para testar os endpoints da API.

## Desafio

O desafio consiste em criar uma tela de login e, após o login bem-sucedido, redirecionar o usuário para uma tela de listagem de produtos. A tela de listagem deve permitir filtros por código, departamento ou descrição.

## Submissão do Desafio
Após a conclusão do desafio, pedimos que você siga os passos abaixo para submeter sua solução:

Disponibilize o Código no GitHub:

1. Crie um repositório público no GitHub para o seu projeto.
   * Envie o Link do Repositório:

2. Envie o link do seu repositório para devteam@lojasnalin.com.br até a data limite de submissão.
   * Instruções de Execução:

3. Inclua no README do seu repositório instruções claras sobre como executar e testar a aplicação.
   * Avaliação:
     A equipe avaliadora irá revisar seu código e fornecer feedback, caso necessário.

Agradecemos pela sua participação e estamos ansiosos para revisar a sua solução!

## Como Testar a API

1. Clone este repositório em sua máquina local.
2. Importe a coleção do Postman "Estágio Nalin.postman_collection.json" para o seu ambiente do Postman.

## Endpoints da API

### Login

**Endpoint:**
- **Método:** GET
- **URL:** [https://api.lojasnalin.com.br:4000/estagionalin/login?ds_login=ESTAGIONALIN&ds_senha=3ST@G10N@L1N](https://api.lojasnalin.com.br:4000/estagionalin/login?ds_login=ESTAGIONALIN&ds_senha=3ST@G10N@L1N)

**Resposta:**
```json
{
    "statuscode": 200,
    "message": "Login efetuado com sucesso",
    "data": [
        {
            "ds_login": "ESTAGIONALIN",
            "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9....",
            "expires_in": 1703117247405
        }
    ]
}
```

### Listagem de Produtos
**Endpoint:**
- **Método:** GET
- **URL:** [https://api.lojasnalin.com.br:4000/estagionalin/produtos/listar]
Parâmetros:

codigo (opcional): Código do produto para filtro.
departamento (opcional): Departamento do produto para filtro.
Resposta:

```json
{
    "statuscode": 200,
    "message": "Sucesso",
    "data": [
        {
            "codigo": 2,
            "descricao": "Produto 2",
            "departamento": "Roupas",
            "valor": "49.99"
        },
        {
            "codigo": 7,
            "descricao": "Produto 7",
            "departamento": "Roupas",
            "valor": "79.99"
        },
        {
            "codigo": 11,
            "descricao": "Produto 11",
            "departamento": "Roupas",
            "valor": "69.99"
        },
        {
            "codigo": 14,
            "descricao": "Produto 14",
            "departamento": "Roupas",
            "valor": "89.99"
        },
        {
            "codigo": 18,
            "descricao": "Produto 18",
            "departamento": "Roupas",
            "valor": "59.99"
        }
    ]
}
```
