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

Criar um novo repositório com método POST, chame uma URL http://localhost:3333/repositories/ e informe o corpo da requisição:

Corpo da requisição:

JSON

````sh
{
	"title": "Desafio 01",
	"url": "https://github.com/Rocketseat/bootcamp-gostack-desafios/tree/master/desafio-conceitos-nodejs",
	"techs": [
		"NodeJS",
		"React"
	]
}
````

Ele retorna todos os projetos cadastrados e o que acabou de ser cadastrado:

JSON

````sh
{
    "id": "b5fe2f8a-32c2-44a1-89ef-7d089d21481f",
    "title": "Desafio 01",
    "url": "https://github.com/Rocketseat/bootcamp-gostack-desafios/tree/master/desafio-conceitos-nodejs",
    "techs": [
        "NodeJS",
        "React"
    ],
    "likes": 0
}
````

Buscando todos os repositórios registrados, método GET, chame um URL http://localhost:3333/repositories/

Ele retorna todos os repositórios cadastrados:

JSON

````sh
[
    {
        "id": "f6b6e9de-bd64-4306-9ca7-b18c0a2551f4",
        "title": "Desafio 01",
        "url": "https://github.com/Rocketseat/bootcamp-gostack-desafios/tree/master/desafio-conceitos-nodejs",
        "techs": [
            "NodeJS alterando",
            "React alterando"
        ],
        "likes": 3
    },
    {
        "id": "89e52368-6fa9-4b57-8046-1b4ac569b9b9",
        "title": "Desafio 02",
        "url": "https://github.com/Rocketseat/bootcamp-gostack-desafios/tree/master/desafio-conceitos-nodejs",
        "techs": [
            "NodeJS",
            "React"
        ],
        "likes": 0
    }
]
````
Alterando um repositório cadastrado de acordo com o código informado, método PUT, chame um URL http://localhost:3333/repositories/ Código do repositório


````sh
http://localhost:3333/repositories/89e52368-6fa9-4b57-8046-1b4ac569b9b9
````

Corpo da requisição:

JSON
````sh
{
	"title": "Desafio 2",
	"url": "https://github.com/Rocketseat/bootcamp-gostack-desafios/tree/master/desafio-conceitos-nodejs",
	"techs": [
		"NodeJS"
	]
}
````

Ele retorna todos os repositórios registrados, in:

JSON

````sh
{
	"id": "89e52368-6fa9-4b57-8046-1b4ac569b9b9",
	"title": "Desafio 02",
	"url": "https://github.com/Rocketseat/bootcamp-gostack-desafios/tree/master/desafio-conceitos-nodejs",
	"techs": [
	    "NodeJS"
	],
	"likes": 0
}
````

Excluindo um repositório registrado de acordo com o código informado, método DELETE, chame um URL http://localhost:3333/repositories/ Código do repositório


````sh
http://localhost:3333/repositories/89e52368-6fa9-4b57-8046-1b4ac569b9b9
````

Ele retornou o código de sucesso:

````sh
200
````

Para dar like no repositório com método POST, chame uma URL http://localhost:3333/repositories/b5fe2f8a-32c2-44a1-89ef-7d089d21481f/like:

Ele retorna o repositório com o número de likes atribuidos a ele:

JSON

````sh
{
    "id": "b5fe2f8a-32c2-44a1-89ef-7d089d21481f",
    "title": "Desafio 01",
    "url": "https://github.com/Rocketseat/bootcamp-gostack-desafios/tree/master/desafio-conceitos-nodejs",
    "techs": [
        "NodeJS",
        "React"
    ],
    "likes": 5
}
````

<br />
Feito com ♥ by Kayza :wave:
