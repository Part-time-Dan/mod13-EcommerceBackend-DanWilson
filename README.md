[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://choosealicense.com/licenses/mit/)

# ORM E-commerce Back End

Object-Relational Mapping of back end API using Express.js, MySQL and Sequelize.

## Description

This project is an Express.js web application simulating back end management of the routing and relational mapping of data to an online shop. The API calls to a database using Sequelize extended model classes to display or update tables for products, tags and categories. 

Specific criteria for this project were to link a handful of models using Sequelize syntax and foreign keys through best-practice file structuring and code out the API logic to GET, POST, PUT and DELETE for most models. Starter code was provided to handle everything outside the criteria objectives.


## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Contributions](#contributions)
- [Questions](#questions)
- [License](#license)
- [Video/Demos](#demo)

## Installation

- VScode (or equivalent program) 

- Insomnia (recommended to view API functionality)

- MySQL Server

- Dependencies: Node.js, mysql2, Sequelize, Express.js
    ```sh
    npm install
    ``` 


## Usage

Clone this repository to a development environment like VScode. Install dependencies listed above.

Start up a MySQL connection `mysql -u root -p` and enter personal credentials. A config file is provided to handle ".env" files as well.

**WARNING: VERIFY YOU DO NOT CURRENTLY HAVE AN ACTIVE DATABASE CALLED "ecommerce_db" BEFORE CONTINUING TO THE NEXT STEP.**

From MySQL terminal, enter `source db/schema.sql` to create the "ecommerce_db" database. Once the database has been created, exit MySQL `quit`.

The /seeds folder contains the index.js file to populate the tables using `npm run seed` or `node seeds/index.js`. The terminal should console log that data has been seeded in the database.

Set up should be complete. Run `node server.js` from the root directory. The console should log that the port is now listening. Open Insomnia and enter 1 of 3 options into the address bar to test the back end routing with GET, POST, PUT and DELETE methods:

- http://<area>localhost:3001/api/categories/
- http://<area>localhost:3001/api/tags/
- http://<area>localhost:3001/api/products/ (Note: POST and PUT methods were provided as starter code for "products")

A 200 status with JSON objects or messages should be returned in the Preview window. For "GET by id", PUT and DELETE methods, include the id number as the search parameter after the last slash in the address (Example- to DELETE category id: 4 "Hats", address should appear as: DEL http://<area>localhost:3001/api/categories/4). 

If the user chooses invalid options or the code has any errors, user should receive 404 or 500 status.


Here is some sample JSON to copy into Insomnia for POST and PUT checks:
```sh
Category POST
{
	"category_name": "Accessories"
}

Category PUT
{
	"category_name": "Candy"
}


Tag POST
{
	"tag_name": "style"
}

Tag PUT
{
	"tag_name": "modern"
}


Product POST
{
      "product_name": "Basketball",
      "price": 200.00,
      "stock": 3,
      "tagIds": [1, 2, 3, 4]
}
```

## Contributions

This is an educational project. No contributions are being accepted.
 

## Questions

If you have questions about this project:

Find me on GitHub -> [Part-time-Dan](https://github.com/Part-time-Dan)

OR

Reach me by email here -> [danielwilson.web@gmail.com](mailto:danielwilson.web@gmail.com)


## License

License information here: [MIT](https://choosealicense.com/licenses/mit/)

## Demo

https://github.com/Part-time-Dan/mod13-EcommerceBackend-DanWilson/assets/126934952/11389b65-b49b-4127-ab6e-c8c98b0f794f
