# Desafio 01 - Banco de Dados Postgresql

Você está dando os primeiros passos no uso de containers. E a melhor forma de iniciar no mundo de containers é usar em ambiente de desenvolvimento.

Sua missão é ajudar a equipe de desenvolvimento a ter mais autonomia no desenvolvimento de projetos. E uma das reclamações da equipe é o setup local.

Crie um comando para criar um banco de dados PostgreSQL no ambiente do desenvolvedor de uma forma que cumpra os seguintes requisitos:

O nome do banco de dados deve ser curso_docker
O usuário de acesso ao banco deve ser docker_usr
A senha do usuário deve ser docker_pwd
Lembrando que a execução em container deve ser transparente pra quem está desenvolvendo. E que aqui você não precisa se preocupar com a perda dos dados do banco e nem nada disso, é apenas para desenvolvimento pontual.

Coloque aqui embaixo o comando que a equipe deve usar pra criar um banco de dados PostgreSQL com esses requisitos.

### Comando para criar o banco de dados com os requisitos solicitados
`docker run --name postgres_db -e POSTGRES_DB=curso_docker -e POSTGRES_USER=docker_usr -e POSTGRES_PASSWORD=docker_pwd -p 5432:5432 -d postgres`

### Comando para acessar o banco de dados
`psql -h localhost -U docker_usr -p 5432 postgres`


# Desafio 02 - Banco de Dados MySQL

Agora que a equipe tem como criar o banco de dados Postgre, crie o comando pra criar o banco de dados MySQL usando os requisitos abaixo:

O nome do banco de dados deve ser docker_db
O usuário de acesso ao banco deve ser docker_usr
A senha do usuário deve ser docker_pwd
Lembrando que a execução em container deve ser transparente pra quem está desenvolvendo. E que aqui você não precisa se preocupar com a perda dos dados do banco e nem nada disso, é apenas para desenvolvimento pontual.

Coloque aqui embaixo o comando que a equipe deve usar pra criar um banco de dados MySQL com esses requisitos:
### Comando para criar o banco de dados com os requisitos solicitados
`docker run --name mysql_db -e MYSQL_DATABASE=docker_db -e MYSQL_USER=docker_usr -e MYSQL_PASSWORD=docker_pwd -e MYSQL_ROOT_PASSWORD=root_pwd -p 3306:3306 -d mysql`

### Comando para acessar o banco de dados
`mysql -h 127.0.0.1 -P 3306 -u docker_usr -pdocker_pwd`


### Desafio 03 - Banco de Dados MongoDB
Pra finalizar essa etapa, crie o comando pra criar o banco de dados MongoDB usando os requisitos abaixo:
O usuário root do banco deve ser mongo_usr
A senha do usuário root deve ser mongo_pwd
Lembrando que a execução em container deve ser transparente pra quem está desenvolvendo. E que aqui você não precisa se preocupar com a perda dos dados do banco e nem nada disso, é apenas para desenvolvimento pontual.

Coloque aqui embaixo o comando que a equipe deve usar pra criar um banco de dados MongoDB com esses requisitos:
### Comando para criar o banco de dados com os requisitos solicitados
`docker run --name meu_mongo -e MONGO_INITDB_ROOT_USERNAME=mongo_usr -e MONGO_INITDB_ROOT_PASSWORD=mongo_pwd -p 27017:27017 -d mongo`

### Comando para acessar o banco de dados
`mongosh -u mongo_usr -p mongo_pwd --authenticationDatabase admin --host 127.0.0.1 --port 27017`
