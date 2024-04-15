# 🚀SynthAI API #
Esse repositório 
👥 **Integrantes do Grupo:**

- RM98163 - Júlia Martins Santana Figueiredo
- RM550562 - Larissa Akemi Iwamoto
- RM98893 - Marcelo Henrique Góes da Costa Borgas
- RM98370 - Ricardo Brito Ponticelli Prieto
- RM94679 - Vinicios Becker Prediger

👤 **Responsaveis pelo projeto**

- RM98370 - Ricardo Brito Ponticelli Prieto

## [🎬Link do vídeo]() ##

## 📊Diagrama de Classe/Modelo Lógico 
<img src="./markdown/diagrama de classes.png">
<img src="./markdown/diagrama modelo logico.png">

## 📋Endpoints da API ##

Verbo|Tipo da requisição	|Descrição
|--|--|--|
Empresa|	GET	|Obtém todas as empresas cadastradas
Empresa/{id}|	GET|	Obtém os dados de uma empresa específica
Empresa	|POST|	Cria uma nova empresa
Empresa/{id}|	PUT	|Atualiza os dados de uma empresa
Empresa/{id}	|DELETE|	Apaga uma empresa

### [📥Requisições](Requisições.jason) ###

## Exemplos ##
### Obter todas as empresas ###

GET 'Empresa'

Retorno:
''' json
[
  {
  "id": 1,
  "cnpj": "60.701.190/0001-04",
	"email": "empresa1@email.com",
	"endereço": "Rua ABCS, 1",
	"nome": "Empresa A"
  },
  
  {
  "id": 2,
  "cnpj": "60.746.948/0001-12",
	"email": "empresa2@email.com",
	"endereço": "Rua EFG, 2",
	"nome": "Empresa B"
  }
]


Status code	|Mensagem
|--|--|
200	|Dados retornados com sucesso

### Obter empresas por ID ###
GET 'Empresa/1'

Retorno:
''' json
[
  {
  "id": 1,
  "cnpj": "60.701.190/0001-04",
	"email": "empresa1@email.com",
	"endereço": "Rua ABCS, 1",
	"nome": "Empresa A"
  }
  
]

Status code|	Mensagem
|--|--|
200|	Dados retornados com sucesso
404	|Empresa não encontrado

### Criar Empresa ###
POST 'Empresa'

Request body:
''' json
[
  {
  "cnpj": "60.701.190/0001-04",
	"email": "empresa1@email.com",
	"endereço": "Rua ABCS, 1",
	"nome": "Empresa A"
  }
  
]

Retorno:
''' json
[
  {
  "id": 1,
  "cnpj": "60.701.190/0001-04",
	"email": "empresa1@email.com",
	"endereço": "Rua ABCS, 1",
	"nome": "Empresa A"
  }
  
]

Status code	|Mensagem
|--|--|
200|	Cliente cadastrado com sucesso

### Atualizar empresa ###
PUT 'Empresa/1'

Request Body:
''' json
[
  {
  "id": 1,
  "cnpj": "60.701.190/0001-04",
	"email": "empresa1@email.com",
	"endereço": "Rua ABC, 1",
	"nome": "Empresa A"
  }
  
]

Retorno:
''' json
[
  {
  "id": 1,
  "cnpj": "60.701.190/0001-04",
	"email": "empresa1@email.com",
	"endereço": "Rua ABC, 1",
	"nome": "Empresa A"
  }
  
]

### Apagar empresa ###
DELETE 'Empresa/2'

Status code	|Mensagem
|--|--|
200	|Empresa deletada com sucesso
404	|Empresa não encontrada
