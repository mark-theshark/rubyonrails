# Ruby on Rails application

This Ruby on Rails "RoR" application lets people in an organization to give feedback and rank it using a "thumbs up" approach.

###### Languages, frameworks used:

* Ruby 3.2.3

* Ruby on Rails 7.3.2.2 (upgraded & tested on 2024-04-07)

* SQLite3

* jQuery JavaScript library 3.3.1

* Bootstrap CSS for styling 4.2.1

* Devise gem for authentication

* will_paginate gem to handle split rows returned across pages

* acts_as_votable gem to up vote a feedback item

* 3 relational tables: users, posts, votes

###### Notes / To run this app after cloning, we recommend:

* use an image or `rbenv` with with Ruby 3.2.3

* install bundler gem then bundle install the gems specified in the gem file

* install the Ruby gems ( they are not in my git to save space ): bundle install

 (the following 2 steps may be needed if you get database errors when launching the rails app)

* run the database migrations: rails db:migrate RAILS_ENV=development

* run the seed data including login user names: rails db:seed

 * launch the app from the app folder: rails s -p 3000 -b 0.0.0.0

 ( the binding lets you access the app outside your localhost )

 * If running in a container, make sure you specify the ports in the docker run to setup port forwarding )

 * log in with the username admin@friends.com and password of password

 * API call #1 to demo in a browser: http://(your app host name)/api/get_posts_count.json

 * API call #2 to demo in a browser: http://(your app host name)/api/get_posts.json?term=

###### DISABLED debugging gems for now - bundling failed

 * start debugger command: rdebug-ide --host 0.0.0.0 --port 1234 --dispatcher-port 1234 -- bin/rails s

 * create a launch.json in VS Code that listens for r-debug

 * make a breakpoint and start the debugger in VS Code, go to the app's route in a browser where the breakpoint is set, and it should break



