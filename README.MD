# Pré-requisitos

- docker
- docker-compose

# Executar o projeto

Clonar o projeto

`$ git clone git@github.com:dfsantos/node-nginx.git`

Vá para a pasta do projeto

`$ cd node-nginx`

Inicie os serviços via docker-compose

`$ docker-compose up -d`

# Validação

## APP Node

Após alguns segundos, deve ser possível acessar uma página no navegador pelo endereço http://localhost:3000. Significa que a aplicação Node está executando corretamente.

## Integração com MySQL

Ao iniciar, a aplicação Node gera um registro na tabela `people` do MySQL. Para validar, siga os passos:

Acessar o container do MySQL

`$ docker exec -it db bash`

Conectar no banco

`$ mysql -uroot -p`

Informar a senha (root):

`$ > root`

Acessar o banco de dados:

`$ > use nodedb;`

Verificar dados na tabela people:

`$ > SELECT * FROM people;`
