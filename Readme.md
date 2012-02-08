Creating a Stasis App with a Custom Stasis Buildpack on Heroku Cedar (from GitHub)
===

Setup Stasis
---

Install the stasis gem

    gem install stasis

Clone the git repository
---

    git clone git@github.com:markpundsack/stasis-example-on-heroku.git
    cd stasis-example-on-heroku
    
Let's test it locally
---

    stasis -d 3000

Open your browser and go to http://localhost:3000.

You should see "Hello World".

Deploying to Heroku
---

Install the Heroku gem

    gem install heroku

Create a Heroku app using our custom buildpack

    heroku create --stack cedar --buildpack http://github.com/markpundsack/heroku-buildpack-stasis.git
    
Deploy!

    git push heroku master

Test it:

    heroku open