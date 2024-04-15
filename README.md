# 🚀SynthAI API #
Esse repositório trás a parte inicial referente as empresas na seção do projeto referente ao Aproveitamento das Oportunidades de Vendas, que analisa os dados dos clientes e utiliza algoritmos de recomendação para identificar oportunidades de venda cruzadas e adicionais. Dessa forma, são oferecidos produtos ou serviços extras que atendam às necessidades e preferências individuais de cada cliente. Esse processo resulta em uma experiência mais personalizada e relevante, aumentando as taxas de conversão e otimizando as receitas.
O restante será reservado para apresentar nas Sprints seguintes do Challenge.

👥 **Integrantes do Grupo:**

- RM98163 - Júlia Martins Santana Figueiredo
- RM550562 - Larissa Akemi Iwamoto
- RM98893 - Marcelo Henrique Góes da Costa Borgas
- RM98370 - Ricardo Brito Ponticelli Prieto
- RM94679 - Vinicios Becker Prediger

👤 **Responsaveis pelo projeto**

- RM98370 - Ricardo Brito Ponticelli Prieto

## [🎬Link do vídeo](https://youtu.be/VYRM56kuzSs) ##

## 📊Diagrama de Classe/Modelo Lógico 
<img src="./diagramas/diagrama de classes.png">
<img src="./diagramas/diagrama modelo logico.png">

## 📋Endpoints da API ##

Verbo|Tipo da requisição	|Descrição
|--|--|--|
Empresa|	GET	|Obtém todas as empresas cadastradas
Empresa/{id}|	GET|	Obtém os dados de uma empresa específica
Empresa	|POST|	Cria uma nova empresa
Empresa/{id}|	PUT	|Atualiza os dados de uma empresa
Empresa/{id}	|DELETE|	Apaga uma empresa

### [📥Requisições](Requisições.json) ###

## Exemplos ##
### Obter todas as empresas ###

GET `Empresa`

Retorno:
```json
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
```

Status code	|Mensagem
|--|--|
200	|Dados retornados com sucesso

### Obter empresas por ID ###
GET `Empresa/1`

Retorno:
```json
[
  {
  	"id": 1,
  	"cnpj": "60.701.190/0001-04",
	"email": "empresa1@email.com",
	"endereço": "Rua ABCS, 1",
	"nome": "Empresa A"
  }
  
]
```

Status code|	Mensagem
|--|--|
200|	Dados retornados com sucesso
404	|Empresa não encontrado

### Criar Empresa ###
POST `Empresa`

Request body:
```json
[
  {
  	"cnpj": "60.701.190/0001-04",
	"email": "empresa1@email.com",
	"endereço": "Rua ABCS, 1",
	"nome": "Empresa A"
  }
  
]
```
Retorno:
```json
[
  {
  	"id": 1,
	"cnpj": "60.701.190/0001-04",
	"email": "empresa1@email.com",
	"endereço": "Rua ABCS, 1",
	"nome": "Empresa A"
  }
  
]
```

Status code	|Mensagem
|--|--|
200|	Cliente cadastrado com sucesso

### Atualizar empresa ###
PUT `Empresa/1`

Request Body:
```json
[
  {
  	"id": 1,
  	"cnpj": "60.701.190/0001-04",
	"email": "empresa1@email.com",
	"endereço": "Rua ABC, 1",
	"nome": "Empresa A"
  }
  
]
```

Retorno:
```json
[
  {
  	"id": 1,
  	"cnpj": "60.701.190/0001-04",
	"email": "empresa1@email.com",
	"endereço": "Rua ABC, 1",
	"nome": "Empresa A"
  }
  
]
```

### Apagar empresa ###
DELETE `Empresa/2`

Status code	|Mensagem
|--|--|
200	|Empresa deletada com sucesso
404	|Empresa não encontrada
