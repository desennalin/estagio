# Desafio de Desenvolvimento - Estágio Nalin

Este repositório contém uma API desenvolvida para o desafio de estágio na Nalin, juntamente com uma coleção do Postman para testar os endpoints da API.

## Desafio

O desafio consiste em criar uma tela de login e, após o login bem-sucedido, redirecionar o usuário para uma tela de listagem de produtos. A tela de listagem deve permitir filtros por código, departamento ou descrição.

## Como Testar a API

1. Clone este repositório em sua máquina local.
2. Importe a coleção do Postman disponível [aqui](https://orange-satellite-630151.postman.co/workspace/NALIN~d55be685-6684-48a1-903a-269d6614028a/collection/27431475-9f064d42-fd51-4c98-951e-5e94e5a9d3ab?action=share&source=collection_link&creator=27431475) para o seu ambiente do Postman.

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
