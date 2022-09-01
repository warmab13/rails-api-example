# README

This repo is based on this link tutorial
[Medium Tutorial](https://medium.com/@oliver.seq/creating-a-rest-api-with-rails-2a07f548e5dc)

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* New project rails
    rails new rest-api-guide --api --database=postgresql
* Ruby version
    3.0.0
* System dependencies
    Generic ruby dependencies ROR project
* Configuration
    Create new model on database: 
    rails generate model User username:string password:string
    rails generate model Fact user:references fact:string likes:integer
    user:references make a foreing key to user, Fact belongs to User and user can have a lot of facts
* Database creation
    You need to have installed postgresql on system and runing to setup database you can use this command with brew installed:
    brew install postgres
    before you create the project.
* Database initialization
    rails db:setup
    rails db:migrate

* How to create controllers 
    rails g controller api/v1/Users
    rails g controller api/v1/Facts

* How to create records on console
    run rails c
     oliver = User.create( username: 'Oliver', password: 'password' )
     fact_one = Fact.create( fact: 'Wiley Hardeman Post was the first pilot to fly solo around the world.', likes: 1, user_id: 1 )
     fact_two = Fact.create( fact: 'The Symphony No1 in E flat major, K.16, was written by Wolfgang Amadeus Mozart at the age of 8.’ likes: 2, user_id: 1 )
* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
