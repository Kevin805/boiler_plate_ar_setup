# Let's Hike App!


## Table of contents
* [General Information](#general-info)
* [Video](video)
* [Technologies](#technologies)
* [Setup](#setup)
* [Features](#features)
* [Status](#status)
* [Contact](#contact)
* [License](#license)

## General Information
Let's Hike is a CLI application that allows users to create a profile/login and search a database of listed hikes. Hikes range from easy to hard as well as short to long.  
Let's Hike allows several ways to find the right hike. You can search specifically by the amount of time you have, 
or allow the app to pick a random hike for you. To find the perfect hike tailored for you, try out our Hike compatibility quiz!
All of these hikes can be saved in your 'favorites' to easily reference in the future.


## Intro Video

## Technologies
* Ruby - version 2.6.1
* ActiveRecord - version 6.0
* Sinatra - version 2.0
* Sinatra-activerecord - version 2.0
* SQLite3 - version 1.4


## Setup
To run the app, install it locally by cloning the GitHub repository and typing:
```ruby
ruby runner.rb
```


## Code Examples
``` ruby
def display_each_trail_name
    puts 'Here is our list of Colorado hiking trails:'
    Trail.all_trail_names.each do |trail_name|
    puts trail_name
    end
  end
end 
```

``` ruby
def ask_difficulty
    system "clear"
    @difficulty_choice = prompt.select("Choose your desired hike difficulty", %w(Easy Medium Hard))
    matching_trails = Trail.where(difficulty: @difficulty_choice)
    puts "You chose #{@difficulty_choice}, saving to your preferences.."
    sleep(1)
end
```

## Features
* Browse Hikes based on length of time.
* Have the app return a random hike for you.
* See Hike details
* Save your favorite hikes
* Use the Hike compatibility quiz to find the perfect hike.


## Status
Project is: finished with option to expand features and further refactor code.


## Contact
Created by [Augie Menos](https://www.linkedin.com/in/augie-menos-9b8329b1/) and [Kevin Johnson](https://www.linkedin.com/in/kevin-johnson805/)


## License
