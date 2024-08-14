⚠️ 🚧 Em andamento 🚧 ⚠️

Feito o clone do arquivo, realize as seguintes instalações via terminal.

npm init -y
npm install sequelize mysql2
npm install --save-dev sequelize-cli
npx sequelize-cli init
npx sequelize-cli model:generate --name Personagem
 --attributes nome:string,ataque:integer,defesa:integer

Após executar a sequência de comandos, é necessário configurar a conexão com o banco
de dados no arquivo config.json.

“development”: {
 “username”: “root”, “password”: “admin123”,
 “database”: “jogo_dev”, “host”: “127.0.0.1”,
 “dialect”: “mysql”
},

A senha é a mesma definida na instalação do MySQL e o database é alterado de acordo com a sua preferência. 

O sequelize-cli deve ser utilizado para criar o banco de dados e a tabela de
personagens, utilizando os comandos da listagem seguinte.

npx sequelize-cli db:create
npx sequelize-cli db:migrate

Lembrando aqui que estamos utilizando
um servidor Express, com suporte a CORS e utilização de Body Parser.

npm install express body-parser cors


O cliente.js é baseado em Axios e a única configuração necessária é a instalação
da biblioteca em um projeto NodeJS.

npm init -y
npm install axios