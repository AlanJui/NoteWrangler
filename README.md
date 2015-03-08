Getting Started
---------------

To get you started you can simply clone the note-wrangler repo and install the dependencies:

### Install Dependencies

You will need node.js installed to run this sample app, I recommend [Node Version Manager](https://github.com/creationix/nvm). Check out the repo for installation directions: [nvm github](https://github.com/creationix/nvm)

-	Install the server side node libraries we depend upon via `npm`, the [node package manager](https://www.npmjs.org/).

We have preconfigured the app using `npm` to automatically run `bower` so we can simply do:

```
npm install
```

This creates a `node_modules` folder which contains the npm packages installed in the previous step

### Run the Application

We have preconfigured the project with a simple development web server. The simplest way to start this server is:

```
npm start
```

Now pull up your application at `http://localhost:8000/`. The default user is `demo` with a password of `secret`

Enable debug mode in Node process
---------------------------------

### Start app in debug mode

```
npm run debug
```

This starts the app in debug mode which allows you you to use [node-inspector](https://github.com/node-inspector/node-inspector) You can open another browser tab at: `http://127.0.0.1:8080/debug?port=5858` to get to the web console.

### Start app in debug mode and pause script on the first line

```
npm run debug-brk
```

### Trouble shooting for can not start app in debug mode

Error Message:

```
Cannot start Node Inspector: EADDRINUSE
There is another process already listening at 0.0.0.0:8080.
Run  '/Users/AlanJui/workspace/yo-angular/NoteWrangler/node_modules/.bin/node-debug -p {port}' to use a different port.

```

Solution:

1.	Get the PID of the node process:

```
  $ pgrep -l node
  2793 node
```

1.	Kill process

```
  $ kill 2793
```

Additional Resources
--------------------

For more information on AngularJS and other kick-butt languages check out [Code School](https://www.codeschool.com/)!
