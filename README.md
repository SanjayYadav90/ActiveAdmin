# ActiveAdmin
Go to you project file and open gemfile. Add followint gems in this file.

  gem 'activeadmin', github: 'activeadmin'
  gem 'devise'

Run bundle to install the gem in your project

  bundle

Run following command form terminal to install active admin

  rails generate active_admin:install 
We will get instruction to make changes in config file

  open file config/environments/development.rb:

  config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }
if we dont have any root the create it by 
  
  rails g controller home index

add following code in rought.rb

  root to: "home#index"

use migration for DB

  $> rake db:migrate
Start server by typing  
  $> rails server

Now you can view admin by typing
  base_url/admin
and provide 
  user id : admin@example.com
  password: password

you will get logged in

If you want to generate new mode in admin then type 

  $> rails generate active_admin:resource [MyModelName]
  
for more detail follow

http://activeadmin.info/docs/3-index-pages.html

