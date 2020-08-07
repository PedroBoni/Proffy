# Server(API REST) - Instructions 📝  
🔧  Built in Node.JS  
Supports all databases, visit http://knexjs.org/ for more information

## Funcionalidades

- ### Conexões
  - Rota para listar o total de conexões realizadas;
- ### Aulas  
  - Rota para criar uma aula;
  - Rota para listar aulas;
    - Filtrar po matéroa, dia da semana e horário;
<h2 id="install">Install</h2>

- Clone this repository and and install the dependencies

    - `npm install`  or  `yarn install`

- Start the database  

  - `npm knex:migrate` or `yarn knex:migrate`

<h2 id="usage">Usage</h2>

- Start   
  - `npm start` or `yarn start`

- To test the features use one of the following tools: 

  - [Postwoman](https://postwoman.io/) - Browser
  - [Insomnia](https://insomnia.rest/download) - Multiplataform (64 bits)
  - [Postman](https://www.postman.com/) - Multiplataform (< 32 bits)

- Resources 
  - GET `/classes` - List to classes
    This feature lists the classes according to the filter
    request URL example:
    ```
    domainname.com/classes?subject=Hist%C3%B3ria&week_day=1&time=10%3A00
    ```
    Querys:  
    - subject  
    - week_day
    - time

  - POST `/classes` - Create a class  
    This feature creates a class and a user  
    request body example:

    ```
    {
        "name": "Leandro Karnal",
        "avatar": "encurtador.com.br/stBGQ",
        "whatsapp": "999999999",
        "bio": "Leandro Karnal é um historiador brasileiro, professor da Universidade Estadual de Campinas, e da PUC-RS, especializado em história da América, escritor, palestrante e apresentador de TV.",
        "subject": "História",
        "cost": 800,
        "schedule":  [
            {
                "week_day": 1,
                "from": "10:00",
                "to": "14:00"
            },
            {
                "week_day": 2,
                "from": "13:00",
                "to": "18:00"
            },
            {
                "week_day": 3,
                "from": "15:00",
                "to": "17:00"
            }
        ]
    }
    ```
  - GET `/connections` - Returns total connections

  - POST `/connections` - Create a new connection
    request body example:
    ```
    {
      "user_id": 1
    }
    ```







