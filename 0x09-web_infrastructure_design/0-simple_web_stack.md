steps:

DNS:

1. The user sends a request to their Internet Service Provider (ISP) to access www.foobar.com.
2. The ISP, which has a resolver server, searches for the requested URL in its resolver. If it finds the URL, it sends back the IP address associated with it.
3. If the URL is not available in the resolver server, the resolver asks the root server for assistance.
4. The root server responds by providing the address of the Top-Level Domain (TLD) server responsible for all the domains of ".com" to the resolver.
5. The resolver then sends a request to the TLD server, which returns the correct domain name after removing the "www." prefix (using either CNAME or A records), along with the address of the authoritative name server.
6. The resolver sends a request with the URL to the authoritative name server, which possesses all the information about the requested URL, including the IP address of the server hosting it.
7. The authoritative name server responds by providing the IP address of the requested server to the resolver server.
8. Finally, the resolver sends back this IP address to the client, which can then send the request to access the site.

The steps involved in ACCESSING THE SITE after the IP address is returned to the client:

9. The client then sends an HTTP or HTTPS request to the server with the correct IP address, which in this case is 8.8.8.8. This server is the one hosting the web server software, such as Nginx.

10. The web server searches for the requested data in its static database. If the data is found, it sends back an HTTP response to the client. The data requested through HTTP typically includes HTML, CSS, JS, images, files, and more.

11. Additionally, the web server may send a request to the application server. The application server handles the dynamic content of the site and manages the application logic, data manipulation, and user requests separately from the web server. It plays a crucial role in handling the dynamic aspects of the website.

It's important to note that the primary role of the web server is to handle HTTP requests from clients, especially for static content.
