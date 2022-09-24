## Introduction
- Node is a **runtime environment** for executing JS code.
- Essentially, Node is a **C++ program that embeds Chrome’s v8 engine**, the fastestJS engine in the world.
- We use Node to build fast and scalable networking applications. It’s a perfect choice for building RESTful services.  
- Node applications are single-threaded. That means a single thread is used to serve all clients.  
- Node applications are **asynchronous or non-blocking by default.** That means when the application involves I/O operations (eg accessing the file system or the network), the thread doesn’t wait (or block) for the result of the operation. It is released to serve other clients.
- This architecture makes Node **ideal for building I/O-intensive applications.**
- node monitor **'event queue'** in background when its find a event in the queue it will take it out and process.
- This kind of architecture makes node ideal for building application that **include lot of disk or network access.** We can serve more clients without the need of more hardware, thats why node app are highly scalable.
- You should avoid using Node for CPU-intensive applications, such as a video encoding service. Because while executing these operations, other clients have to wait for the single thread to finish its job and be ready to serve them.
- In Node, we don’t have browser environment objects such as window or the document object. Instead, we have other objects that are not available in browsers, such as objects for working with the file system, network, operating system, etc.
- RESTAPI - Representational State Transfer

### What's special in Node JS
- Node is easy to get started and can be used for prototyping and agile development.
- But I can also used to develop superfast and highly scalable services  its used in large company like paypal, uber, netflix.
- With Node we can build twice as fast with fewer people.
- 33% fewer lines of code.
- 40% fewer  files.
- Its double the no of request per sec **2* request/sec***
- Frontend developer can also reuse javascript code.
- Large ecosystem of open source libs

### Node Module system
Global object in JS are:

```js
console.log();
setTimeOut();
clearTimeOut();
setInterval();
clearInterval();
```

### Modules
- Module refer to a .js or .tsx files.
```js
var url = " ";

function log() {
console.log("message");
}

module.export.log = log;
module.export.baseurl = url;

```

#### Module wrapper function
- Every module always wrap in a function.
```js
(function(export, require, module, filename){
	var url = "";
	module.exports = url;
})
```


### env 
- set environment variable using
```
# mac cmd
export PORT=5000

[[windows]] cmd
Set PORT=5000
```

### Packages
[[Packages for Node JS]]

## Initial setup
