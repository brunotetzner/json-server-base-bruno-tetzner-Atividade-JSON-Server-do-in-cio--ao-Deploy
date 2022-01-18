# json-server-base

Esse é o repositório com a base de JSON-Server + JSON-Server-Auth já configurada, feita para ser usada no desenvolvimento das API's nos Capstones do Q2.

Na presente atividade foi desenvolvida uma API simples voltada para estudantes, onde eles podem cadastrar as matérias que estão estudando ou que tem interesse em estudar no futuro.
Também é possivel adicionar assuntos que o estudante está vendo naquela matéria.

## Endpoints

Assim como a documentação do JSON-Server-Auth traz (https://www.npmjs.com/package/json-server-auth), existem 3 endpoints que podem ser utilizados para cadastro e 2 endpoints que podem ser usados para login.

### Cadastro

POST /register <br/>
POST /signup <br/>
POST /users

Qualquer um desses 3 endpoints irá cadastrar o usuário na lista de "Users", sendo que os campos obrigatórios são os de email e password.
Você pode ficar a vontade para adicionar qualquer outra propriedade no corpo do cadastro dos usuários.

### Login

POST /login <br/>
POST /signin

Qualquer um desses 2 endpoints pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"

### Matérias:

O usuário pode criar ou visualizar matérias de outros usuários.

Aviso: É necessário estar logado para criar uma matéria, no entanto, qualquer um pode visualiza-las.
Visualizar Matérias: GET /subject

Criar uma matéria:
É necessário informar, o titulo, a descrição e o seu id de usuário para criar uma matéria

POST /subject

#### Assuntos:

Referem-se aos assuntos que o usuário estuda em cada matéria. Somente usuários logados podem visualiza-los.

Visualizando seus assuntos:
GET /topic

Criando um assunto:

POST /topic
É necessário informar um titulo, o id de usuário, e o id da Matéria.
