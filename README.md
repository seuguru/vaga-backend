![seuguro](http://www.seuguru.com.br/email/logo.gif)


## Simulador de Seguro
 - Criar um endpoint para cadastro e visualização do usuario e simulação do produto de seguro de vida.
 - A entrega deve ser via github, enviar o repositório

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
```json
{
  "user_id": 1,
  "risk_type": "Prédio Comercial",
  "address": "Rua Faria Lima"
  "number": "250",
  "zipcode": "04315001"
}
```
