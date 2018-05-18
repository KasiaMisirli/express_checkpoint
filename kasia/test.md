# Node/Express Test

### Question 1

What is `module.exports` and why do we use it?

```text
this is an object. module is a variable that reperesents current module and exports is an object exposed to the module. this can be assigned to function or object that we want to be used in another file
```

### Question 2

Write one Express route for each of the four CRUD actions.

Then, make each route respond with a one-word string containing the RESTful action that would most likely be associated with this route.

```js
var express = require("express")
var app = express()

app.get('/', function (request, response) {
  res.send("read")
})

app.post('/quotes', (req, res) => {
  res.send('create')
})

app.get('/', (req, res) => {
  res.send("find")
})

app.put('/name/update/:id', (req, res, next) => {
    res.send("update")
})
```
app.delete('/name/delete/:id', (req, res, next) => {
    res.send("delete")
});
### Question 3

Describe the differences between Express and Rails as backend frameworks.

```text
Your answer...
```

### Question 4

What do the following lines of code do?

```js
var bodyParser = require("body-parser")
app.use(bodyParser.json())
app.use(bodyParser.urlencoded({extended: true}))
```

```text
Your answer...
```

### Question 5

For this exercise you will be creating an es6 BankAccount class.

It will have the following properties...
* `type` (e.g., "checking"), which should be determined by some input
* `balance`, which should start out as `0`

It should have the following methods...
* `withdraw`, which should decrease the balance by some input
* `deposit`, which should increase the balance by some input
* `showBalance`, which should print the balance in the bank to the console.

The `BankAccount` class has a `transactionHistory` property which keeps track of the withdrawals and deposits made to the account.
* Make sure to indicate whether the transaction increased or decreased the amount of money in the bank.

```text
Your answer...
```

Create an instance of the BankAccount class

```text
Your answer...
```
