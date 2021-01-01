# Tombardier Backend

Tombardier - Portfolio Building Made Simple

A browser based portfolio builder for developers to quickly build and deploy a personal site


Built with a Ruby on Rails API backend(this file), and a React/Redux front-end for Flatiron School Software Engineering Program


## Installation

Once you fork and clone this repo

Simply run bundle install to install tombardier's frontend.

```bash
bundle install
```

# Getting Started with Tombardier Backend

Start up your rails server and enjoy

```bash
rails s
```

# Heroku

- Download and install the Heroku CLI.
-https://devcenter.heroku.com/articles/heroku-cli


then:
```bash
heroku create
git push heroku main
heroku run rake db:migrate
heroku run rake db:seed
```


# Integrating AWS


# Rails Credentials 

```EDITOR='code --wait' rails credentials:edit```

You should something like this: 
    aws:
    access_key_id: 123
    secret_access_key: 345

    # Used as the base secret for all MessageVerifiers in Rails, including the one protecting cookies.

    secret_key_base: 3a6666666fef1bf8f18dad3bb609411a0f0ba1ddc1ce9e5a65d11ec089b6cc1f15ffd3cdd496f2cd3cb5a8051f4cdf29876ac65816a70f5a155e0798f86614aa

If you dont, double check you used the correct command

Comment out Line 32 in Config/Production.rb



then add this:
"# Store files on Amazon S3.
  config.active_storage.service = :amazon"


reset heroku db: heroku pg:reset DATABASE