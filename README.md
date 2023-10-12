# Understanding Client-Server Architecture with MySQL as RDBMS
Client-Server Architecture with MySQL as the Relational Database Management System (RDBMS) is a system where multiple computers (clients) interact with a dedicated computer (server) to store and retrieve structured data managed by MySQL. The server acts as a centralized data organizer, while clients can request, modify, or add information based on MySQL's rules. This setup is commonly used in web applications to ensure efficient data management and access.


## Client-Server Architecture
Client-Server Architecture is like teamwork in computers. Clients ask for things, and servers give them. It helps organize how computers work together, making things efficient and easy to manage on a network.

A simple example of Client-Server interaction is shown below:

`curl -Iv www.propitixhomes.com`

Client: In this case, my local broser acts as the client, and is responsible for initiating the communication, making requests to a server, and receiving responses. The client uses thee curl command to achieve this interaction.

Server: The server, in this case, is the web server that hosts the website www.propitixhomes.com. It is responsible for listening to incoming requests, processing those requests, and sending back responses. The IP address "75.2.115.196" and port 80 are the server's address and port where the server is listening for incoming HTTP requests.

`-I` This option tells curl to send an HTTP HEAD request, which requests only the headers of the web page and not the full content. It is often used to check for server response and header information without downloading the actual page content.

`-v` This option stands for "verbose" and tells curl to be more verbose, providing additional information about the request and response, including progress details, request headers, and response headers.

So, when you run this command, curl sends an HTTP HEAD request to www.propitixhomes.com and displays the response headers in a verbose manner. This is useful for checking the HTTP headers of a web page, which can provide information about the server, content type, response status, and other important metadata without downloading the entire page content.

![Client-Server Architecture](./Images/1.png)

This output is the verbose output of the curl command when you run curl -Iv www.propitixhomes.com. It shows the various stages of the HTTP request being made. Here's a breakdown of the output:

* Trying 75.2.115.196:80...: curl is attempting to connect to the IP address 75.2.115.196 on port 80. This is the initial step where it establishes a connection with the web server.

* Connected to www.propitixhomes.com (75.2.115.196) port 80 (#0): The connection to www.propitixhomes.com at the specified IP address and port 80 is established, and curl has assigned it the identifier "0" for this request.

> HEAD / HTTP/1.1: This line shows the HTTP request being sent. It's a HEAD request for the root path ("/") using HTTP version 1.1.

> Host: www.propitixhomes.com: This is part of the HTTP request header, specifying the "Host" header with the hostname of the website you're accessing.

> User-Agent: curl/7.81.0: This is another part of the HTTP request header, indicating the user-agent string, which identifies the client making the request. In this case, it's curl version 7.81.0.

> Accept: */*: This part of the HTTP request header specifies that the client (curl) can accept any type of content ("/").

## Implement a Client Server Architecture using MySQL Database Management System (DBMS)

