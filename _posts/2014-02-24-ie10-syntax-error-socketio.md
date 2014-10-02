---
layout: post
title: IE10 throws syntax error when its client socket.io is trying to connect to a NodeJS server
...

It's [clearly documented][1] that websocket is supported in IE10. Numerous blog
posts have shown sample chat applications using NodeJS and socket.io and have
never mentioned anything about any issue with IE10. So when I get the following
syntax error thrown by IE10, I got not much help from google.

[1]: <http://caniuse.com/#search=websocket>

The reason that the web has not reported on this issue, I think, is because most
sample chat application, in order to illustrate the concept of using socket.io
do not have the sample app configured to run on port 80.

If you look in the source code of socket.io.js, when the following line

```JavaScript
this.websocket = new Socket(this.prepareUrl() + query);
```

is executed, the value returned by this.prepareUrl() is

```
ws://connect5.codeprototype.com:/socket.io/1/websocket/3mKnD1xZvY8Rv97Mf_8S
```

Notice that the port number is left at blank if it's 80. All of the 'nice'
browsers, i.e. Chrome, FireFox, Safari can handle that syntax just fine. IE10,
even though it supports websocket, decides to be a pain in the neck by
complaining it's a syntax error. To fix this, we just have to make sure that
port number 80 is explicit like this:

```
ws://connect5.codeprototype.com:80/socket.io/1/websocket/3mKnD1xZvY8Rv97Mf_8S
```

This is one of those situations where figuring out what the root cause of the
problem took 99% of the time, and to fix the problem, it took the remaining 1%.
But I'll take this over the reverse situation any day. Anyway, the fix is fairly
simple:

<script src="https://gist.github.com/pragmaticlogic/9182946.js"></script>
