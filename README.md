# Todo MVC 
<img src="https://github.com/tastejs/todomvc/blob/master/media/logo.png">

This is an example implementation of TodoMVC, which was developed to showcase typical usage of the [Transcendent.js](https://github.com/ldaniels528/transcendent.js) platform 
(a Scala.js implementation of the Node SDK and MEAN stack).

For more details, please refer to the documentation of the original project:

https://github.com/tastejs/todomvc

This project is comprised of 3 sub-projects:
* AngularJS project (angularjs)
* NodeJS project (nodejs)
* A common project (commonjs) for shared classes

## Building the code

<a name="Build_Requirements"></a>
#### Build Requirements

* [Scala 2.11.8+] (http://scala-lang.org/download/)

**NOTE:** You'll also need to have a working installation of the Node package manager (npm) and bower.

#### Building the application

Prior to building the code, you need to install the bower and node modules. 
*NOTE*: You only need to perform this step once.

```bash
$ cd app-nodejs
$ npm install
$ bower install
$ cd ..
```

Now, you can compile the Scala.js sources to JavaScript by executing the following command:

```bash
$ sbt clean "project nodejs" fastOptJS
```

**NOTE:** If you'd like continuous compilation (to recompile as you change the source code) then do the following instead:

```bash
$ sbt clean "project nodejs" "~ fastOptJS"
```

#### Running the application

```bash
$ cd ./app-nodejs
$ node ./server.js    
```

**NOTE:** To run Node if development mode, do the following instead:

```bash
$ cd ./app-nodejs
$ NODE_ENV=development node ./server.js    
```

The above will startup the application on port 1337 by default. To listen/bind to a different port. Set the "port" environment
variable.

```bash
$ NODE_ENV=development port=8000 node ./server.js
```

Then (re)start the application.

<img src="https://github.com/ldaniels528/transcendent-js-todomvc/blob/master/todo-mvc-screenshot.png">