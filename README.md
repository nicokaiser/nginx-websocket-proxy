# nginx WebSocket Proxy

As of version 1.4, nginx is capable of forwarding WebSocket requests, so it can be used as a reverse proxy for HTTP, HTTPS, WS and WSS.

Here are some simple example configuration snippets for WebSocket forwarding in nginx.

## Requirements

* nginx 1.4.x or higher
* WebSocket and HTTP server running on `ws|http://localhost:8080`

This is a typical scenario given by [Engine.IO](https://github.com/LearnBoost/engine.io), [Socket.IO](https://github.com/LearnBoost/socket.io), [Primus](https://github.com/primus/primus), etc. which provide a WebSocket server with HTTP fallback.


## Example Configs

* [Simple WebSocket Proxy](simple-ws.conf) – forwards WS and HTTP requests to `ws|http://localhost:8080` 
* [WebSocketSecure Proxy](simple-wss.conf) – forwards WSS and HTTPS requests to `ws|http://localhost:8080`
* [WebSocket Proxy with Path Rewriting](path-rewriting.conf) – forwards `wss|https://ws.example.com/services/myservice` to `ws|http://localhost:8080`
* [WebSocket Proxy with Load Balancing](load-balancing.conf) – like previous example, but with three backend servers, with one client always being forwarded to the same backend


## See Also

* http://nginx.org/en/docs/http/websocket.html
* [Nginx Server Configs](https://github.com/h5bp/server-configs-nginx) – Great resource for nginx server config documentation


## Author

**Nico Kaiser**

+ http://twitter.com/nicokaiser
+ http://kaiser.me
+ http://github/nicokaiser


## License

[MIT License](LICENSE.md)
