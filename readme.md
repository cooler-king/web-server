WebServer
=========

An efficient server library for quickly creating a WebServer and handling HTTP requests, WebSocket
connections, and API requests in the Dart language.

Includes extra nice features, such as setting a parameter to require Basic Authentication for a Urls,
with all of the difficult auth checking and responding taken care of by the server.

~~~dart
// Initialize the WebServer  
final WebServer localWebServer = new WebServer(InternetAddress.LOOPBACK_IP_V4, 8080,
      hasHttpServer: true, hasWebSocketServer: true);
      
// Attach HttpServer pages and event handlers
localWebServer.httpServerHandler
    // Automatically parse for indexing and serve all recursive items in this directory matching the accepted file types.
    ..serveVirtualDirectory('/web/', const <String>['html', 'css', 'dart', 'js']);
~~~