 <h1>Donate-API</h1>
 <hr>
<p>Este é o backend da aplicação Donate - O objetivo dessa aplicação é conseguir cadastrar animais e possíveis doações para os respectivos seres.</p>
<hr>

<h2>Endpoints:</h2>
<p>A API conta com 5 endpoints: em que se todos forem executados o usuário podrá efetuar o Login, cadastrar um animal que necessita de doações e consequentemente realizar doações de diversos valores.</p>

<h2>Endpoints que não precisam de autenticação:</h2>
<ul>
<li> Login;</li>
<li> Get Animals;</li>
</ul>

<hr>

<h2>Endpoints que precisam de autenticação:</h2>
<ul>
<li> New Animal;</li>
<li> New Donation;</li>
<li> Get Donations;</li>
</ul>

<h1>Login:</h1>

`POST /login -  FORMATO DA RESPOSTA - STATUS 200`
```json
{
  "accessToken": "eyJhJMztjc...",
  "user": {
    "email": "kenzinho@mail.com",
    "name": "Kenzinho",
    "age": 38,
    "id": 1
  }
}
```
<h1> New Animal </h1>

`POST /animals - FORMATO DA ENTRADA - STATUS 201`
```json
{
  "name": "Méra",
  "type": "cachorro",
  "userId": 1
}
```
<h4>Bearer: token</h4>
<hr>

`POST /animals -  FORMATO DA RESPOSTA - STATUS 201`
```json
{
  "name": "Méra",
  "type": "cachorro",
  "userId": 1,
  "id": 2
}
```
`GET /animals - FORMATO DE RESPOSTA - STATUS 200`
```json
[
  {
    "name": "Ayra",
    "type": "cachorro",
    "userId": 1,
    "id": 1
  },
  {
    "name": "Méra",
    "type": "cachorro",
    "userId": 1,
    "id": 2
  }
]
```
<h4>Este endpoint não necessita de um Body como entrada.</h4>
<hr>

<h1>New Donation</h1>

`POST /donations -  FORMATO DA ENTRADA - STATUS 201`
```json
{
"value": 150
}
```
<h4>Bearer: token</h4>
<hr>

`POST /donations -  FORMATO DA RESPOSTA - STATUS 201`
```json
{
  "value": 140,
  "id": 3
}
```
`GET /donations - FORMATO DE RESPOSTA - STATUS 200`
```json
[
  {
    "value": 100,
    "id": 1
  },
  {
    "value": 350,
    "id": 2
  },
  {
    "value": 140,
    "id": 3
  }
]
```
<h4> Bearer: token</h4>
<h4>Este endpoint não necessita de um Body como entrada.</h4>
<hr>

<h5>Feito por: <a href = "https://github.com/gabrielguti" target = '_blank'>gabrielguti.</a></h5>
