# Week One - Module 4 Recap

Fork this repository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR.

### What's the most useful thing you learned from completing the intermission week work?

The intermission work itself was underwhelming. I worked through six JS exercisms and the first 10 of Wes Bos' "Javascript 30" course, found it very helpful. Perhaps include it in future week's pre-work?

Our first two days of JS in class could have been pre-work too.

This would make for quite a bit more pre-work, but I would have preferred that.

### What are some tools to help debug JavaScript code?

PryJS, 'debugger'.

### What are some tools you need in order to unit test your JavaScript?

mocha and chai

### What is the syntax for invoking a function?

```javascript
myCoolFunction()
```

### What's the difference between == and === in JavaScript?

`==` is an equality operator
`===` is "deep equality", and useful when `==` fails. (I don't recall more than this. I always reach for `==`)

### What's the difference between asynchronous and synchronous JavaScript?

most JS is synch. That's why for tests you're always adding `function(done)` all over, to let the whole test run before the test finishes.

AJAX is asynch, and lets you keep "open" functions while waiting for stuff to finish.

Asynch JS keeps you out of callback hell, along with promises (`.then()`)

### How do we setup a route when creating an API with Node and Express?

```javascript
var app = express()

app.get('/', function(request, response){
  // do some stuff here.
})
```

### What do we use Knex for?

Databases!


### What's npm and what do we use it for?

Node Package Manager, aka Rail's gem ecosystem.

`package.json` is Node's version of Rail's `Gemfile`



## Review

### What's the MVC design pattern? Describe each part of MVC?

Model View Controller

Model handles most of the logic of the app

View presents things to the user

Controller handles "routing" inside the app.

Lots of nuance to it, but that's the basic gist.


### What is AJAX? What are some benefits of using AJAX?

Asynchronous JavaScript X.... something.

Lets you move data between browser > server w/o a page refresh. So, sorta bare minimum for pleasing-to-use websites.



### What's a background worker? When would we want to use a background worker?

Ruby is synchronous, and if you have it issue a task (like, when a user signs up, they should receive a welcome email) it'll sit there and wait until the task finishes.

So, to keep the app speed up, any time you're sending a task out, assign it to a background worker, who will work through it on its own time.

Appropriate for: email operations, big DB operations, anything.
