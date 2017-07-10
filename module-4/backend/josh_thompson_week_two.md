## Week Two - Module 4 Recap - Josh Thompson



Note: When you're done, submit a PR. 

### What is Webpack and why is it useful?

Handles "packaging" all of our files for delivery to the browser.

It packs all our JS into a single file, removes whitespace and unneeded characters, etc.

This reduces the size and number of requests the user's browser needs to make to load up the data.

### When do you want to use event delegation?

Lets us watch for "child" events, and catch new changes. (Instead of attaching an event listener to every row, we can tell it's parent to have the event listener, and to rely on event delegation)


### What's one difference between ES5 and ES6?

arrow functions

String interpolation



### What's the deal with semi-colons in JavaScript?

They're generally unneeded

### How are you using the MVC design pattern in your Quantified Self project?

Building up food/meal models, moving DB interactions into "services", etc. 

Our "controller" (aka server) is still super obese, but... whatever.

### How do you execute raw SQL in node?

`database.raw(sql here)`

### What's a callback function and what are some reasons when we use/need callback functions?

JS is asynchronous, so functions would (otherwise) finish before we got all the data they needed.

The callback keeps it "open" until the expected function is called, at the end of the code block.


### What is CORS?

Cross Origin ... scripting?

It's passing data along to an untrusted source. I think it was originally a large attack surface for websites.

### What are some steps to avoid CORS?

Er, so far I've avoided only getting blocked by cors, by following short guides online...



#### Review  

### Why do people say "HTTP is stateless"?

Server doesn't know the "state" of the client. Everything is (from the server's perspective) a series of unconnected request/response cycles. 

### What is a RESTful API?

It sticks to the HTTP verbs. 

### What are some main characteristics of a team following an agile workflow?

Regular commits, iterative development. clean code?


### What are some advantages/disadvantages to using OAuth to authenticate a user?

Pros: We don't have to roll our own crypto, can rely on work someone else has done, users might prefer to sign in with a known service instead of creating a new account.

cons: we dont' get to control the login/signup experience as well, can't get as much data from the user as we might want
