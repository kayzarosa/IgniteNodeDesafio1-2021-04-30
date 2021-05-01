<h1 align="center">
    <img alt="Desafio: Conceitos do Node.js" src="https://user-images.githubusercontent.com/20192309/116768782-a4243600-aa0f-11eb-8a25-50d44d27eecc.png" width="100%" />
</h1>

## Desafio: Conceitos do Node.js

# :rocket: Back-End

> TUDO ESTÁ BEM!!!!!.  <img src="https://user-images.githubusercontent.com/20192309/80777643-4202cd80-8b3c-11ea-8f32-5348bda4486b.jpg" width="10%" />

## Sobre o projeto

Uma aplicação para treinar os conceitos básicos do NodeJS apreendidos até o momento no curso, como trabalhar com uuid, arrays, entre outras funcionalidades.


## Versão e instalação

<a href="https://nodejs.org/pt/"> NodeJS 14.15.1 LTS</a> <br/>

## Ou pode instalar o NVM no linux que você pode trabalhar com qualquer versão do node.

<a href="https://github.com/nvm-sh/nvm"> NVM</a> <br/>


Proxímo passo é baixar o gerenciador de pacotes <a href="https://classic.yarnpkg.com/en/docs/install#debian-stable">Yarn </a> é só seguir os passos no site, observação: a versão a ser instalada deve ser a versão estável.
<br />

## Instalação dos pacotes

Instale todas as dependências do projeto com o comando abaixo:

````sh
yarn
````

## Iniciar uma API

````sh
yarn dev
````

## Usando a API

Criar um novo usuário com método POST, chame uma URL http://localhost:3333/users/ e informe o corpo da requisição:

Corpo da requisição:

JSON

````sh
{
  "name": "Kayza",
  "username": "Kayza"
}
````

Será retornado os seguintes dados caso seja sucesso:

JSON

````sh
{
    "id": "6ae1782b-15b1-4ff5-90d7-98d0c59c95d7",
    "name": "Kayza",
    "username": "Kayza",
    "todos": []
}
````

Para todas as requisições que forem feitas a partir daqui devem term em seu Headers o seguinte parametro:

````sh
username: nome do usuário que esta buscando e trabalhando
````

Criar um novo todo para o usuário encontrado no Headers com método POST, chame uma URL http://localhost:3333/todos/ e informe o corpo da requisição:

Corpo da requisição:

JSON

````sh
{
    "title": "Teste 1",
    "deadline": "2021-04-30"
}
````

Será retornado os seguintes dados caso seja sucesso:

JSON

````sh
{
    "id": "a7c71fb1-2621-4506-ba20-2011a39b0d48",
    "title": "Teste 1",
    "done": false,
    "deadline": "2021-04-30T00:00:00.000Z",
    "created_at": "2021-05-01T02:34:16.837Z"
}
````

Buscando todos os todos registrados, método GET, chame um URL http://localhost:3333/todos/

Ele retorna todos os todos cadastrados para o username encontrado no Headers:

JSON

````sh
[
    {
        "id": "c74d8a45-0b9f-4a65-9dc5-663d38b414d7",
        "title": "Teste 1",
        "done": false,
        "deadline": "2021-04-30T00:00:00.000Z",
        "created_at": "2021-05-01T02:34:14.558Z"
    },
    {
        "id": "3c61b069-d4d3-480a-b4a9-50b5f4285e61",
        "title": "Teste 2",
        "done": false,
        "deadline": "2021-04-30T00:00:00.000Z",
        "created_at": "2021-05-01T02:34:15.337Z"
    }
]
````

Alterando um todo cadastrado de acordo com o código informado e o username do Headers, método PUT, chame um URL http://localhost:3333/todos/id Código do todo


````sh
http://localhost:3333/todos/be6bbb14-6c04-4bf4-be51-6aa1ab17e550
````

Corpo da requisição:

JSON
````sh
{
    "title": "Teste 2",
    "deadline": "2021-04-30"
}
````

Irá retornar as alterações realizadas:

JSON

````sh
{
    "id": "be6bbb14-6c04-4bf4-be51-6aa1ab17e550",
    "title": "Teste 2",
    "done": false,
    "deadline": "2021-04-30T00:00:00.000Z",
    "created_at": "2021-05-01T02:34:16.837Z"
}
````

Excluindo um todo registrado de acordo com o código informado, método DELETE, chame um URL http://localhost:3333/todos/ Código do todo


````sh
http://localhost:3333/todos/89e52368-6fa9-4b57-8046-1b4ac569b9b9
````

Ele retornou o código de sucesso:

````sh
204
````

Para mudar o status do done do todo usamos a requisição PATCH, chame uma URL http://localhost:3333/todos/b5fe2f8a-32c2-44a1-89ef-7d089d21481f/done:

Ele retorna o repositório com o número de likes atribuidos a ele:

JSON

````sh
{
    "id": "be6bbb14-6c04-4bf4-be51-6aa1ab17e550",
    "title": "Teste 2",
    "done": true,
    "deadline": "2021-04-30T00:00:00.000Z",
    "created_at": "2021-05-01T02:34:16.837Z"
}
````

<br />
Feito com ♥ by Kayza :wave:
