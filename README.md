![seuguro](http://www.seuguru.com.br/email/logo.gif)


## Simulador de Seguro
 - Criar usuarios e autenticação (EXTRA)
 - Criar um endpoint para cadastro de seuguros
 - Criar endpoint para cadastro de cobertura
 - Criar endpoint para listagem dos seguros e suas coberturas.
 - Criar um endpoint para cotação de seguros.
 - A entrega deve ser via github, enviar o repositório


## Como calcular o custo da cobertura?
  CAPITAL: Valor quanto o usuario gostaria de assegurar.
  PREMIO: Valor que o deve pagar para ter o seguro.

  Você deve multiplicar o (capital * fator) para calcular o **premio**

## Entidades
  
  - Seguros
  - Coberturas
### Seguro

| id  | nome  |
|---|---
|  1 | seguro de vida  |
|  2  | seguro residencial

### Coberturas


| id  | seguro_id  | nome | fator |
|-----|------------|------|-------|
|  1 | 1  | Morte Acidental  | 0.2|
|  2  | 1 | Invalidez permanente | 0.9 |
|  3  | 2 | Quebra de Vidros | 0.2 |
|  4  | 2 | Vendaval | 0.1 |


## Tecnologia
- Utilizamos NodeJS, Express, TypeScript, TypeORM mas fique a vontade para enviar o seu teste na linguagem que preferir.

### [POST] /api/users
request
```json
{
  "name": "John Doe",
  "age": 23,
  "address": "Av. Pres. Juscelino Kubitschek",
  "number": "12",
  "zipcode": "05021000"
}
```

### [GET] /api/users/:id
response
```json
{
  "id": "2",
  "age": 32
}
```

### [POST] /api/simulator 
request
```json
{
  "user_id": 1,
  "insurance_id": 1,
  "coberturas": [
    {coverage_id: 1, capital: 100000}
  ]
}
```
response
```json
{
  "insurance_id": 1,
  "coverages": [
    {coverage_id: 1, name: "Morte Acidental" capital: 100000, premio: 100 }
  ],
  "total": 123.0
}
```