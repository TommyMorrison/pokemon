# Introduction to Node

## What is Node?

- the makers of nodejs took javascript (confined to a browser) and allowed it to run on your computer.
- basically,
* javascript originally run within the browser.
* it can only really access your web page.

Now,

nodejs gives js an enviornment to run on your local machine.

- access files
- listen to network traffic
-  listen to http requests that your machine might get and send back a file
-  anything you can do with php and ruby on rails, you can now do it with js in nodejs.


## What can you do with NodeJS?
There are 2 categories of what you are able to do with node.
1. build utilities on your machine - unilities for dayin/dayout development. ex: gulp, grunt, yeoman, etc.
2. web server / web application (instead of using PHP, ruby on rails, python we use express framework for nodejs, koa framework for nodejs)



## The basics
### Executing js files
- go into the directory containing the file you want to execute
- run 'node filename'


### What are modules?
* modules are how you load one file into another using require.
* pass variables and functions between files using reqire and exports



### How modules work
**programOne.js**

    var m2 = require('./programTwo.js');

    console.log(m2);

**programTwo.js**

    var welcome = "Welcome to the play ground!";

    module.exports.welcome = welcome;
    exports.bye = 'bye!'

Now, require and export a function:

**programOne.js**

    var m2 = require('./programTwo.js');
    var m3 = require('./programThree.js')

    console.log(m2);

    m3();

**programTwo.js**

    var welcome = "Welcome to the play ground!";

    module.exports.welcome = welcome;
    exports.bye = 'bye!'

**programThree.js**

    var welcome = 'Hello welcome to node!'

    module.exports = function() {
        console.log(welcome);
    }

### NPM Modules
NPM - **N**ode **P**ackage **M**anager.
- it allows you to download and manage packages

Example:

* npm install underscore

**programOne.js**

    var m2 = require('./programTwo.js');
    var m3 = require('./programThree.js')
    var _ = require('underscore')

    console.log(m2);

    m3();

    console.log(_);

* package.json
* npm init
* npm install backbone vs. npm install --save

* Delete Node Module - npm install. don't upload node module to github.


### will go more into Node next week.
