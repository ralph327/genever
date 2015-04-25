genever 
========

`genever` is a simple command line utility for live-reloading Go web applications. Just run `genever` in your app directory and your web app will be served with `genever` as a proxy. `genever` will automatically recompile your code when it detects a change. Your app will be restarted the next time it receives an HTTP request.

`genever` adheres to the "silence is golden" principle, so it will only complain if there was a compiler error or if you succesfully compile after an error.

## Installation

Assuming you have a working Go environment and `GOPATH/bin` is in your `PATH`, `genever` is a breeze to install:

~~~ shell
go get github.com/ralph327/genever
~~~

Then verify that `genever` was installed correctly:

~~~ shell
genever -h
~~~

## Supporting Gin in Your Web app
`genever` assumes that your web app binds itself to the `PORT` environment variable so it can properly proxy requests to your app. Web frameworks like [Martini](http://github.com/codegangsta/martini) do this out of the box.
