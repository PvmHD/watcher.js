watcher.js
=====
[![Build Status](https://travis-ci.org/boboman13/watcher.js.svg)](https://travis-ci.org/boboman13/watcher.js)

> Watcher.js is a server management tool, designed to enable a system admin (or anyone that uses multiple servers) to keep a watch on their servers. It keeps track of uptime, network connections, speed, and more.

The software is written in [Node.js](http://nodes.org "NodeJS"). It is not recommended for use as it is in **heavy development**.

### Configuration
A sample configuration file can be found [here](https://github.com/boboman13/watcher.js/blob/master/app.yml). Here is a brief overview of the settings:
* Settings
	* Daemon: The settings for the daemon include the hostname and the port. Change these to change what the socket listens on. These are necessary if you are running a frontend also.
	* Frontend: The settings for the frontend include just the port to listen on. It will listen on all interfaces regardless.
* Servers
	* Server: A server takes four options: name, host, port, and id. It is necessary to put a `localhost` server if you wish to utilize the frontend server as a registered server, it will not list it automatically. The id should be the same as the list key. Putting the servers are *only necessary for the frontend*.

### Installation
```bash
$ git clone https://github.com/boboman13/watcher.js.git
$ cd watcher.js

$ npm install
$ npm run compile # Compiles the app. Scroll down to Compilation for more information.

$ node watcher
```

### Compilation
Compiling watcher.js requires [CoffeeScript](http://coffeescript.org).
```bash
$ npm -g install coffee-script
$ npm run compile
```

### Contributing
Contributing to watcher.js is easy. Simply fork the repository, commit changes to your own repository, and then pull request the changes. Here is a contributing FAQ.

> Do I need to know CoffeeScript to contribute to watcher.js?

No. CoffeeScript is only used on the backend, and you may contribute to the frontend (Javascript, HTML, CSS) if you know the correct languages.

> Do I need to know how to program to contribute to watcher.js?

No! If you find an issue or want a feature, create a [new issue](https://github.com/boboman13/watcher.js/issues). It'll help us figure out how we can help you.

> Why is watcher.js written in CoffeeScript? Why not just Javascript?

CoffeeScript has an eloquent syntax and favors readability. Not the entire app is written in CoffeeScript, but the language helps cut down on app size and code length by removing trivial characters necessary with Javascript.