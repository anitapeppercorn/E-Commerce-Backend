# E-Commerce Backend
I have built the back end for an e-commerce site. I have used an Express.js API, configure it to use Sequelize to interact with a MySQL database.

Because this application is not deployed, I have created a walkthrough video that demonstrates its functionality. 
1. A link to the video where I seed and start running the application on locallost is here. 
2. I have tested the routes on Insomnia and that Demo is included here https://youtu.be/KlwsOc-TnfQ 
3. This application is deployed to github at: https://github.com/anitapeppercorn/E-Commerce-Backend

## Contents
- [Description](#Description)
- [Demo & Models](#Demo&Models)
- [User Story](#User-Story)
- [Acceptance Criteria](#Acceptance-Criteria)
- [Installation](#Installation)
- [Dependencies](#Dependencies)
- [License](#License)
- [Author](#Author)

## Description

Internet retail, also known as e-commerce, is the largest sector of the electronics industry, having generated an estimated US$29 trillion in 2017 (Source: United Nations Conference on Trade and Development). E-commerce platforms like Shopify and WooCommerce provide a suite of services to businesses of all sizes. Due to the prevalence of these platforms, developers should understand the fundamental architecture of e-commerce sites.


## Demo & Models
![Demo GIF of app](/assets/app.gif)
![DemoVideo](https://youtu.be/KlwsOc-TnfQ)
### Demo 
The video that demonstrates the functionality of the backend and shows the technical acceptance criteria being met. It shows how a user would invoke the application from the command line and a functional menu with the options outlined in the acceptance criteria.
### Database Models
The database should contain the following four models, including the requirements listed for each model:
#### Category
id
    Integer
    Doesn't allow null values
    Set as primary key       
    Uses auto increment

category_name
    String
    Doesn't allow null values
#### Product
id
    Integer
    Doesn't allow null values
    Set as primary key
    Uses auto increment

product_name
    String
    Doesn't allow null values

price
    Decimal
    Doesn't allow null values
    Validates that the value is a decimal

stock
    Integer
    Doesn't allow null values
    Set a default value of 10
    Validates that the value is numeric

category_id
    Integer
    References the category model's id

#### Tag
id
    Integer
    Doesn't allow null values
    Set as primary key
    Uses auto increment

tag_name
    String

#### ProductTag
id
    Integer
    Doesn't allow null values
    Set as primary key
    Uses auto increment

product_id
    Integer
    References the product model's id

tag_id
    Integer
    References the tag model's id

#### Associations
You'll need to execute association methods on your Sequelize models to create the following relationships between them:
1. Product belongs to Category, as a category can have multiple products but a product can only belong to one category.
2. Category has many Product models.
3. Product belongs to many Tag models. Using the ProductTag through model, allow products to have multiple tags and tags to have many products.
4. Tag belongs to many Product models

## User Story
AS A manager at an internet retail company
I WANT a back end for my e-commerce website that uses the latest technologies
SO THAT my company can compete with other e-commerce companies

## Acceptance Criteria
GIVEN a functional Express.js API
WHEN I add my database name, MySQL username, and MySQL password to an environment variable file
THEN I am able to connect to a database using Sequelize
WHEN I enter schema and seed commands
THEN a development database is created and is seeded with test data
WHEN I enter the command to invoke the application
THEN my server is started and the Sequelize models are synced to the MySQL database
WHEN I open API GET routes in Insomnia Core for categories, products, or tags
THEN the data for each of these routes is displayed in a formatted JSON
WHEN I test API POST, PUT, and DELETE routes in Insomnia Core
THEN I am able to successfully create, update, and delete data in my database


## Installation
To use this application: Clone the GitHub repository, and install all the dependencies, with```npm install```, on the integrated terminal install all the dependcies. Create your .env file and type in:
DB_NAME='ecommerce_db'
DB_USER='yourusername'
DB_PW='yourpassword'

In the integrated terminal, seed and start using ``npm start``. Use Insomnia to test out the backend.


### Dependencies
- "dotenv": "^8.2.0",
- "express": "^4.17.1",
- "mysql2": "^2.1.0",
- "sequelize": "^5.21.7"
    

## License
[MIT License](./LICENSE)
![license](https://img.shields.io/badge/License-MIT-blue)

### Author: Anita Ganti
![Badge](https://img.shields.io/badge/Github-anitapeppercorn-4cbbb9) 
![Profile Image](https://github.com/anitapeppercorn.png?size=50)
View the author's portfolio at:  https://anitapeppercorn.github.io/anitaprofileportfolio/


[Table of Content](#Table-of-Content) --- [Back to Top](#E-Commerce Backend) --- [Installation](#Installation)
