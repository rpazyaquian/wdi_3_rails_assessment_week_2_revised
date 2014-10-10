# Rails Commands Quiz

Fork, clone, and write your answers directly in this file. Then submit a pull request.

### Question 1

I want to start a new Rails project/app called `BunnyApp`. What command should I type in the terminal?

  rails new BunnyApp --database=postgresql

### Question 2

I want to create a new model called `Bunny`, with the following attributes: name (string), color (string), and age (integer). What command(s) should I type in the terminal and/or Sublime? (In your answer, create both a migration and the model file.)

  The easy way is to generate a model:

  rails g model Bunny name color age:integer

  That will generate a matching migration file for you.
  You can also generate a migration file:

  rails g migation CreateBunnies name color age:integer

  and place the matching Model file under app/models/bunny.rb.

### Question 3

What does the command in Question 2 do, exactly? What files are created, where are they located, and what does the database look like at this time? Explain.

  A migration file called (timestamp)_create_bunnies.rb is created under db/migrations. The Model file is located at app/models/bunny.rb. The database does not change until migrations are run.

### Question 4

I want to create a database and make it reflect the new model I created in Question 2. What command(s) should I type in the terminal?

  rake db:create db:migrate

### Question 5

I want to look at the actual database that has been created. What command should I type in the terminal?

  rails db
  \dt

### Question 6

I want to see a list of all the URLs available in my app, along with the HTTP requests and controllers associated with them. What command should I type in the terminal?

  rake routes (or show-routes in pry)

### Question 7

What line should I add to `config/routes.rb` to create a complete set of RESTful routes for a "bunnies" resource?

  resources :bunnies

### Question 8

According to standard Rails conventions, what directory and filename would the BunniesController be located in, starting from the root of the project?

  Controllers should be placed under app/controllers. In this case, the location of the Controller will be app/controllers/bunnies_controller.rb.

### Question 9

According to standard Rails conventions, what directory and filename would the "show" view for bunnies be located in, starting from the root of the project?

### Question 10

I have worked on my app and finally want to see it in action. What command should I type in the terminal, and where should I navigate to in my browser?
