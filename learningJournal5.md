Structured Query Language is a kind of programming language that helps to retreive or manupulate data in database.
Poupular databases are SQLite, MySQL, Postgres, Oracle and Microsoft SQL Server.
We can think relational databases as a collection of tables that related with each other. For example we have 2 tables and these two table has same data but with diffrent attributes. If we want to reach these attributes we need to use that data's id which is primary key.
Common sql codes to retreive and manipulate data :
-SELECT column name(if we want to retreive  multiple column we can separate them )
FROM mytable;
-Select * from table name --> retreive all datas from the table.
-SELECT colmn name
FROM table name
WHERE condition( for example if there is a table and this table has people and their age we can put condition to retrive people who is older than 30)

I also learned how to use express package

const bodyParser = require('body-parser').urlencoded({extended: true});
const express = require('express');
const app = express();
const PORT = process.env.PORT || 3000;

Get request and response for server side

app.use(express.static('./public'));

app.get('/new', (request, response) =>
  response.sendFile('new.html', {root: './public'}));

app.post('/articles', bodyParser, function(request, response) {
  console.log(request.body);
  response.send('Record posted to server!!');
});

app.use((req, res) => {
  res.status(404).send('Invaild request');
});

app.listen(PORT, () => console.log(`Listening on port: ${PORT}`));
