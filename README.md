Setting Up Node, Express, MongoDB from scratch

### `Prerequisites`

Install Node js from nodejs(https://nodejs.org/)for more information.

Vs code editor from Visualstudio(https://code.visualstudio.com/)for more information.

VS code setup for web developer (http://rbkpdas.blogspot.com/) for more information.

Install mongodb and compass from https://www.mongodb.com/

Install Compass, the GUI for MongoDB. https://www.mongodb.com/products/compass

Open MongoDB Compass

> click on connect
> click on CREATE DATABASE
> Database Name : my-blog
> Collection Name :articles

Click on create database

> my-blog.articles
> ADD DATA - Insert Document
> Put: {"\_id":{"$oid":"61068be27bbd997b5d738280"},"name":"node-express","votes":1,"comments":[]}
> Insert

Create a folder and open in VS code

Open VS code terminal

> npm init -y

> npm install --save express

> npm install --save-dev @babel/core @babel/node @babel/preset-env

create a file named as .babelrc { "presets": ["@babel/preset-env"]}
Create a file named as src/server.js

import express from 'express';

const app = express();

app.get('/hello', (req, res)=>{
res.send("Welcome to Node, Express, Mongo!");
})

app.listen(8000, () => console.log('Listening on port 8000'));

> npx babel-node src/server.js

browse http://localhost:8000/hello

Welcome Node, Express, Mongo !

> npm install --save body-parser mongodb

> npm install --save-dev nodemon

Update
"scripts": {
"start": "npx nodemon --exec npx babel-node src/server.js" in package.json file

> npm start

Browse or Postman: http://localhost:8000/api/articles/learn-express

Output : {"\_id":"61068be27bbd997b5d738280","name":"learn-express","upvotes":1,"comments":[]}
