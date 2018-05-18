# Node/Express Test

### Question 1

What is `module.exports` and why do we use it?

it is a program which you can use within a file to call a function when it is required, in a separate file for instance.

### Question 2

Write one Express route for each of the four CRUD actions.

Then, make each route respond with a one-word string containing the RESTful action that would most likely be associated with this route.

```js
var express = require("express")
var app = express()

app.listen(PORT, () => {
  console.log(`listening on ${PORT}`)
})

app.use(express.static('public'))

app.get('/', (req, res) => {
res.render('home')
})

```

### Question 3

Describe the differences between Express and Rails as backend frameworks.

Rails is structured and opinionated - you need to abide by its conventions. You download gems to store globally, can be used for multiple projects. Rails is considered slower and synchronous.

Express is less opinionated - gives you more freedom where to place files or commands. You download npms locally for each project as you need them. Node.js is considered faster and async.

### Question 4

What do the following lines of code do?

```js
var bodyParser = require("body-parser")
app.use(bodyParser.json())
app.use(bodyParser.urlencoded({extended: true}))
```
requires the use of an installed middleware module called body-parser
it is accessing data in the form JSON
the data will be posted in a nested object


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

var withdrawnAmount = 0
var depositAmount = 0

class BankAccount {

  constructor(type = 'Savings', balance = 0) {
    this.type = type
    this.balance = balance
  }
   withdraw() {
     balance = this.balance - withdrawnAmount
     return this.balance
   }
   deposit() {
     balance = this.balance += depositAmount
     return this.balance
   }
   showBalance() {
     return this.balance
   }
   get transactionHistory()
   return ???
 }
}




Create an instance of the BankAccount class

BankAccount.showBalance();
