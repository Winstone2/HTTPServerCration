# HTTPServerCration
const http = require('http');
This line imports the built-in Node.js http module. This module provides functionality for creating and interacting with HTTP servers and clients. By requiring 'http', you gain access to the methods and objects provided by the module.
const server = http.createServer((req, res) => {
    res.writeHead(200, {'Content-Type': 'text/plain'});
    res.end('Hello, World!\n');
});
Here, a new HTTP server instance is created using the createServer method from the http module. The createServer method takes a callback function as its argument. This function is called for each incoming HTTP request. Inside this callback:

    The res.writeHead method is used to set the HTTP response status code and headers. In this case, it sets a 200 OK status code and a Content-Type header of 'text/plain'.
    The res.end method sends the response data, which is the string 'Hello, World!\n', back to the client.
    const PORT = 8580; 
const HOST = '0.0.0.0';
These lines define constants for the port and host that the server will listen on. PORT specifies the port number (8580 in this case), and HOST specifies the network interface to bind to. '0.0.0.0' means the server will listen on all available network interfaces.
server.listen(PORT, HOST, () => {
    console.log(`Server is listening on ${HOST}:${PORT}`);
});
inally, the listen method of the server instance is called to start the server and make it listen for incoming connections. It takes the PORT, HOST, and a callback function as arguments. The callback function is executed once the server starts listening. In this case, it simply logs a message indicating that the server is now listening on the specified host and port.

Thought Process:

    Import the http module to access its functionality.
    Create an HTTP server instance using createServer.
    Define the response behavior inside the server callback function.
    Set up constants for the desired port and host.
    Call server.listen to start the server on the specified port and host.
    Output a message indicating that the server is now listening.

When you run this script using Node.js, it will create an HTTP server that listens on the specified port and responds with a "Hello, World!" message for any incoming requests. The server will be accessible on all available network interfaces due to the use of '0.0.0.0' as the host.
