# Catalog
  This is the Udacity Full Stack Web Development project #4
  
  
## About
   This is web application build with python framework flask.This is the informative web app
   which gives information about car models in market
   
   
## Requirements
  - python
  - Flask
  - SQLAlchemy
  - Oauth2client
  - requests
  - Virtualenc
  
  
## How to run server
  In order to run this server you need to install python(2.7) or higher in your machine(linux/windows).


  It is recommended to use vagrant for testing .This will not effect your machine configurations.
  Here is [documentation](https://www.vagrantup.com/docs/) to install vagrant and [virtual box](https://www.virtualbox.org/wiki/Documentation) 
  
  
  The entry point for this project is project.py
  run this file using
  ```
  $python project.py
  
  ```
## Files in this project
  ```
  catalog
  ├── client_secrets.json
  ├── db_setup.py
  ├── carmodels.db
  ├── static
  │   └── style.css
  ├── templates
  │   ├── addCompany.html
  │   ├── addmodel.html
  │   ├── CdeletePrompt.html
  │   ├── deleteModel.html
  │   ├── editCompany.html
  │   ├── editModel.html
  │   ├── head.html
  │   ├── login.html
  │   ├── main.html
  │   ├── showComModels.html
  │   └── viewModel.html
  ├── project.py
  └── README.md
  ```
  - client_secrets.json file contains oauth2 info.
  - db_setup.py is the database setup file which create tables in the sqllite database using sqlalchemy
  - carmodels.db is the sqllite database file
  - static folder contains the static files such as css,javascript,images etc.
  - templates folder contains the html files which is used to render data
  - Project.py is the main file which contains all routes and logic
## Oauth 
  This application authenticates users using Google Oauth v2 api and stores user data in database.
  More [about](https://developers.google.com/identity/protocols/OAuth2) Google Oauth 
  
  
  For this api to work you need to have client_secrets.json which can downloaded from [Google Api Console](https://console.developers.google.con) 
  Then
  - Create a new project
  - Go to credentials page and update your information
  - Download the client_secret.json file and place it project directory
  
### webpage sample
   - [picture1](https://lh4.googleusercontent.com/CCLYRLrtBhc96XYIZxc_up_9kfaI6uQfj1nqF4_rA61h3fBUXGLzWIIfporOFtWDX7EUMFYeWU8VZhtDVdzt=w1960-h3936-rw)
   - [picture2](https://lh3.googleusercontent.com/lqOiOHwnsTwLGLlSnQncVnBbsZhTF_0OjKi-0MhuVyzBP44z54D6slBR2qQrM96stjNYcjKI61vPl0e81QpK=w1960-h3936-rw)

## Api End points
  - [localhost:5000/json](http://localhost:5000/json)
    This will return all the companies details with its models
  - [local:5000/company/<int:c_id>/json](http://local:5000/company/1/json)
    This will return json data of company models
  - [local:5000/company/<int:c_id>/model/<int:model_id>/json](http://localhost:5000/company/4/model/3/json)
    This will return json data model data
