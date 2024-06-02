## 🚀 Projeto Educacional EE Francisco Voccio

Um professor de informática me informou que estava dando aulas de programação para alguns de seus alunos em Java. Portanto me convidou a lessionar uma aula referente a API's e ambientes Web. De cara, aceitei este será o conteúdo principal da nossa aula. Backend.

> Portanto, deixarei este repositório público para que os mesmos consultem.

## ⚙️ API Endpoints

Todas as rotas possuem `api/v1`. Antecendo, como prefixo da rota.

### POST /products

Cria um novo produto. 

**Parâmetros**

| Nome       | Local | Tipo   | Descrição            |
|------------|-------|--------|----------------------|
| `name`     | body  | string | Nome do produto.   |
| `value`    | body  | float64 | Valor do produto.|

**Resposta**

```json
{
    "idProduct": "ca1b4739-ef67-47a4-aa3d-e84c1ed69e11",
    "name": "Gabinete Electrolux v2",
    "value": 120.00
}
```
---

### GET /products

Busca por todos produtos. 

**Resposta**

```json
[
    {
        "idProduct": "d17f6001-b4b0-46bb-8f34-fb0c878b23f4",
        "name": "Monitor Dell 27",
        "value": 4600.00,
        "links": [
            {
                "rel": "self",
                "href": "http://localhost:8080/api/v1/products/d17f6001-b4b0-46bb-8f34-fb0c878b23f4"
            }
        ]
    },
    {
        "idProduct": "e610641c-42ec-4772-8398-63cf6d63fb98",
        "name": "Lavadora LG",
        "value": 250.00,
        "links": [
            {
                "rel": "self",
                "href": "http://localhost:8080/api/v1/products/e610641c-42ec-4772-8398-63cf6d63fb98"
            }
        ]
    },
    {
        "idProduct": "20b26d05-6c8f-4795-b45c-928c0c14d5ec",
        "name": "Gabinete Electrolux",
        "value": 120.00,
        "links": [
            {
                "rel": "self",
                "href": "http://localhost:8080/api/v1/products/20b26d05-6c8f-4795-b45c-928c0c14d5ec"
            }
        ]
    },
    {
        "idProduct": "ca1b4739-ef67-47a4-aa3d-e84c1ed69e11",
        "name": "Gabinete Electrolux v2",
        "value": 120.00,
        "links": [
            {
                "rel": "self",
                "href": "http://localhost:8080/api/v1/products/ca1b4739-ef67-47a4-aa3d-e84c1ed69e11"
            }
        ]
    }
]
```
---
### GET /products/{id}

Busca por um produto baseado em seu id. 

**Parâmetros**

| Nome       | Local | Tipo   | Descrição            |
|------------|-------|--------|----------------------|
| `id`     | url  | string | UUID do produto.   |

**Resposta**

```json
{
    "idProduct": "ca1b4739-ef67-47a4-aa3d-e84c1ed69e11",
    "name": "Gabinete Electrolux v2",
    "value": 120.00,
    "_links": {
        "Products List": {
            "href": "http://localhost:8080/api/v1/products"
        }
    }
}
```
---
### PUT /products/{id}

Altera os dados de um produto baseado no id. 

**Parâmetros**

| Nome       | Local | Tipo   | Descrição            |
|------------|-------|--------|----------------------|
| `name`     | body  | string | Nome do produto.   |
| `value`    | body  | float64 | Valor do produto.|

**Resposta**

```json
{
    "idProduct": "ca1b4739-ef67-47a4-aa3d-e84c1ed69e11",
    "name": "Gabinete Electrolux v2",
    "value": 120.00,
    "_links": {
        "Products List": {
            "href": "http://localhost:8080/api/v1/products"
        }
    }
}
```
---
### DELETE /products/{id}

Deleta um produto baseado no id. 

**Parâmetros**

| Nome       | Local | Tipo   | Descrição            |
|------------|-------|--------|----------------------|
| `name`     | body  | string | Nome do produto.   |
| `value`    | body  | float64 | Valor do produto.|

**Resposta**

```json
{
    "message": "Product deleted successfully"
}
```
