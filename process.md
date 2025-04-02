# 1. Enter the domain name in the address bar
 #### Example

 https://jennapederson.dev/hello-world

 ##### scheme
 `https://` is the protocol used to connect to the website.This is the first part of the URL which tells the browser to connect to the server Using TLS.

 ##### domain name
 `jennapederson.dev` is the domain name of the website. It pointss to a specific server's IP address.

 ##### path
 `/hello-world` is the path to the specific page on the website. This is the second part of the URL which tells the browser where to find the page.

 ##### Resource
 `hello-world` is the name of the page on the website. 

 # 2. Browser Looks up the IP address of the domain name

 The browser needs to figure out which server on the internet to connect to.
 The browser needs to to look up the IP address of the domain name using the DNS.
 DNS data is cached between different layers of the browser and at various places across the internet.

 The browser checks its own cache, the operating system cache, a local network cache at your router, and a DNS server cache on your corporate network or at your internet service provider.

 If the IP is not found in any of the cached data, the DNS server does a recursive DNS lookup, which asks multiple DNS servers around the internet, which in turn ask more DNS servers for the DNS record until found.
Once the ip is found, the browser makes a connection to the server using the IP address.

# 3. Browser initiates TCP connection to the server.
Using the public internet routing infrastructure, packets from a client browser request get routed through the router, the ISP, through an internet exchange to switch ISPs or networks, all using transmission control protocol (TCP)., to find the server with the IP address
Most sites use content delivery network CDN, to cache content closer to the browser to improve performance.

The request is intelligently routed through the most performance location to deliver content to the browser.

The TCP connection is established once the browser finds the server on the internet and if HTTPS is being used, a TLS handshake takes place to secure the communication.

# 4. Browser sends HTTP request to the server

The browser sends a HTTP request to the server to get the page from the server.

The HTTP  request contains a request line, headers and the body


Contents of the request line:
- A request method, such as GET, POST, PUT, DELETE, etc.
- The path , pointing to the requested resources.
- The HTTP version communicating with the server.


Contents of the headers:
- User agent information, such as the browser and operating system.
- Accept header, indicating the types of content the browser can accept.
- Accept-Language header, indicating the preferred languages.
- Referer header, indicating the URL of the page that linked to the current page.
- etc.


# 5. Server processes the request and sends back a response

The server processes the request and sends back a response to the browser.

The response contains a response line, headers and the body.

Contents of the response line:
- a status line, telling the client the status of the request
- response headers, telling the browser how to handle response
- the requested resources at that path, either content like HTML,CSS JS or images or data.

The status line contains both the HTTP version and numeric and text representation of the status code.

```js
HTTP/1.1 200 OK
Date: Tue, 25 May 2021 19:40:59 GMT
Server: Apache
X-Frame-Options: SAMEORIGIN
X-Powered-By: Express
Cache-Control: max-age=0, no-cache
Content-Type: text/html; charset=utf-8
Vary: Accept-Encoding
X-Mod-Pagespeed: 1.13.35.2-0
Content-Encoding: br
Keep-Alive: timeout=1, max=100
Connection: Keep-Alive
Transfer-Encoding: chunked

<!DOCTYPE html>
<html lang="en">
<head>
    THE REST OF THE HTML
</head>

</html>
```
The browser considers a status code in 200s to be a successful response.

# 6. Browser renders the page in the browser for the user to interact.

The browser renders the page in the browser for the user to interact.
The `Content-Type` header above tells the browser it received an HTML resource in thr response body.

The browser then displays the page in the browser for the user to interact.

## Wrapping up

The browser makes a request to the server, the server processes the request and sends back a response. The browser then displays the page in the browser for the user to interact.

The six steps:

1. Type a URL in your browser and press ENTER
2. The browser looks up the IP address of the domain name
3. The browser initiates TCP connection to the server
4. The browser sends HTTP request to the server
5. The server processes the request and sends back a response
6. The browser renders the page in the browser for the user to interact
