# Node/Express Test

### Question 1

What is `module.exports` and why do we use it?

```text
this is an object. module is a variable that reperesents current module and exports is an object exposed to the module. this can be assigned to function or object that we want to be used in another file
Kasun: export code from one file to another,reduce complexity and repitation.
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
})
### Question 3

Describe the differences between Express and Rails as backend frameworks.

```text
Rails is used with Ruby and its a framework that is less flexible in terms of naming files. Rails on default creates files that we should use if we want to follow the convention. Also its seems to require more files then Express. Ruby uses preinstalled gems as long as we specify them in the gemfile. Rails can only be tested in the terminal.We can run it in our local host if we set up the server file. Uses controller files (user_controller.rb). Uses model files ending with erb.


Express is used with NodeJS, aka Javascript and its less "opinionated", meaning has less preset conventions, which makes it more flexible. 
Also, we need to install modules every time we create a new project.
Express can be tested in dev tools. We can run it in our local host if we set up the server file. Doesnt have controller files. Uses model files ending with ejs.
```

### Question 4

What do the following lines of code do?

```js
var bodyParser = require("body-parser")
app.use(bodyParser.json())
app.use(bodyParser.urlencoded({extended: true}))
```

```text
First line require module body parser.
bodyparser: extract the entire body portion of an incoming request stream and exposes it on req.body.
bodyParser.json: Returns middleware that only parses json and only looks at requests where the Content-Type header matches the type option.
bodyParser.urlencoded: Returns middleware that only parses urlencoded bodies and only looks at requests where the Content-Type header matches the type option. 
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
class BankAccount{
  constructor(balance = 0){
    this.balance = balance
    this.history = []
  }
  withdraw(amountW){
    this.balance -= amountW
    this.history.push({type: "w",amount: amountW })
    return balance
  }
  deposit(amountD){
    this.balance += amountD
    return balance
  }
  showBalance(){
    console.log(balance)
  }

}
```
