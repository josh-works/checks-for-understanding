# Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. **List the five common HTTP verbs and what the purpose is of each verb.**
```
  GET: requests data from server
  POST: client "posts" data to server
  DELETE: deletes data from server
  PUT: very similar to POST - I'm still not sure of the difference
  PATCH: <- looked that one up
```


2. **What is Sinatra?**

baby rails. It's a framework written in the Ruby language. 

4. **What is MVC?**

model/view/controller, or the framework's way of handling all the data flows of an application.

5. **Why do we follow conventions when creating our actions/path names in our Sinatra routes?**

Because until I have a good reason not to, I'm gonna always stick with conventions. Also, all the HTTP verbs function as "reserved" words in Sinatra, so if you use `GET`, you get (heh, a joke) all those goodies handed to you automatically. 

6. **What types of variables are accessible in our view templates without explicitly passing them?**

Well, anything available to the object that we pass to the template is available as a variable. And all the objects have any of their rows accessible, so if I have a `station` object, it will be able to access all of it's own variables. 

Technically, I could probably do Active Record queries from inside the View, but I think it's best to keep that logic in the model if possible. 

7. **Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?**
  
  ```ruby
  get '/horses' do
    @count = 1
    erb :index, :locals => {
      :count => @count
    }
  end
  ```
  Or something like that. ^^ didn't look it up, but I know we've done this in our intro to AR repo. 

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

```ruby
name = "Mr. Ed"

get '/horses' do
  @count = 1
  
  erb :index, :locals => {
    :count => @count,
    :name => name
  }
end
```

9. **What's the purpose of ERB?**

Embedded ruby - lets you mix ruby and HTML, for fun and for profit. 

10. **Why do I need a development AND test database?**

TBH, not sure right now. I know they're different, can't pinpoint why, or how I'd use them.

11. **What's responsive design?**

Building a page/app that works in a variety of screen sizes. (Desktop > tablet > mobile)

12. **What is CRUD and why is it important?**

The bread and butter of data management/display is Creating, Reading, Updating, and Deleting it. (CRUD). Most apps out there are nicely (or not nicely) skinned CRUD apps.

13. **What does HTTP stand for?**

HyperText Transfer Protocol (I think.)

14. **What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?**

<%= this_code_will_be_printed_in_the_html %>
<% this_code_will_not_be %>

Use the first for showing data inside of an enumerable., while the second would be to start/end the block.

15. **What's an ORM?**

Object relational mapper. AKA ActiveRecord, plays between our applications and our databases. Converts ruby to SQL. 

16. **What's the most commonly used ORM in ruby (Sinatra & Rails)?**

ActiveRecord. 


17. **Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.**

```
get '/' => show the application root
get '/restaurants' => show all of the restaurants (list)
get /restaurants/:id  => show a specific restaurant
get '/restaurants/:id/edit' => show the page to edit a specific restaurant
put '/restaurants/:id' => the above page would post to the DB to update the restuarant info
delete '/restaurants:id' => delete the restaurant

I don't remember the seventh...
```

18. **What's a migration?**

Runs table SQL queries to add/delete/update/modify tables/values. The end result is the underlying DB structure is different, and `schema.rb` will reflect the changes.

usually looks like: `rake db:create_migration NAME=migration_name` => modify the migration file to do what you want it to do => `rake db:migrate` => view `schema.rb` to confirm that it did what you wanted it to do


19. **When you create a migration, does it automatically modify your database?**

ah, sorta already answered this. No, you have to run the migration. `rake db:migrate`

20. **How does a model relate to a database?**

A model has, at minimum, a 1:1 relationship with a database. If you have a `Restaurants` table, you need a `Restaurant` model. The model is where all the finding/selecting/calculating functions will be written.


21. **What's the difference between agile workflow and waterfall method?**

Agile works, waterfall doesn't. Also, agile is flexible. If you wanted to build a car w/Agile, you'd start with the problem (transportation) and incrementally build from there. I.E. skateboard > scooter > bike > moped > motorcycle > car.

W/waterfall, you'd jump straight to building the car. Hope you don't forget a seatbelt or lug nuts or something. :)


22. **What is the difference between `#new` and `#create`?**

`new` makes an object, but doesn't save it in the DB. (You can verify because the object ID will be `nil`). Create adds the object to the db. If you look at it's ID, it won't be `nil`.
