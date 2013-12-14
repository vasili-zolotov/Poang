[![Build Status](https://strider.aws.paperg.com/524b2794297d256705000009/vasili-zolotov/Poang/badge)](http://strider.aws.paperg.com/vasili-zolotov/Poang/)

## Poang - A sample node.js/MongoDB app for Strider &amp; Heroku/MongoLab

Poang demonstrates a few of the ways that we write tests in Node.js for Strider (Strider is a hosted continuous deployment platform for Node.js and Python. Learn more at [StriderApp.com](http://striderapp.com)).

Poang ([github](https://github.com/BeyondFog/Poang)) is a Node.js/MongoDB app built using the [Express](http://expressjs.com/) framework. Poang uses [Everyauth](http://everyauth.com/) for local authentication, [Mongoose-Auth](https://github.com/bnoguchi/mongoose-auth) to connect Everyauth to MongoDB (and [Mongoose](http://mongoosejs.com/) as the ODM) for account persistence, and [Connect-Mongo](https://github.com/kcbanner/connect-mongo) as a session store. Most of the code in app.js was generated by Express and all of the code in auth.js after the Comment schema is straight from the Mongoose-Auth docs.

For testing, Poang uses the [Mocha](http://visionmedia.github.com/mocha/) test framework, [should](https://github.com/visionmedia/should.js) for assertions, [Sinon.JS](http://sinonjs.org/) for mocks & stubs, and [Zombie.js](http://zombie.labnotes.org/) for lightweight integration testing.

For more details, please see Steve's [blog post](http://blog.beyondfog.com/?p=222) that walks through the various tests in Poang.

## Installation
 
A) To use Poang with Strider, simply fork Poang and then add it to Strider via the 'Add Repo' workflow. Then skip down to 'deploy to Heroku' below.

B) To install Poang on your dev box:

1) Do a git clone:

    git clone git://git@github.com:BeyondFog/Poang.git
    
2) cd into the project directory and then install the necessary node modules:

    npm install -d

3) start up MongoDB if it's not already running:
  
    mongod --noprealloc --nojournal
    
4) start the node process:

    node app.js

## Deploy to Heroku

After you have created a new app on Heroku and pushed the code via git, you will need to use the Heroku Toolbelt from your command line to add the free MongoLab starter addon:

    heroku addons:add mongolab:starter --app [your_app_name]
-----

Strider is a hosted continuous deployment platform for Python and node.js. Learn more at [StriderApp.com](http://striderapp.com)
