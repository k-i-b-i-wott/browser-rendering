# HTTP response status codes

Status codes are used to indicate the status of a request or response.

The status code is a three digit number that indicates the status of the request or response.

## Informational Responses (100-199)

- `100 Continue `- The response indicates that the client should continue the request.
- ``101 Switching Protocols`- The server indicates that it is switching protocols.
- `102 Processing`- The server has received and is processing the request, but no response is available yet.

- `103 Early Hints`- The server is sending hints about the response that will be sent later.

## Successful responses (200-299)

- `200 OK`- Standard response for successful HTTP requests.
  It depends on the HTTP Method
  - `Get`: The resources has been fetched and transmitted in the message body.
  - `HEAD:` Representation headers are included in the response without any message body
  -`PUT or POST:` The resource 
  - `Trace:` The message body contains the request as received by the server

- `201 Created`
 The request succeeded, and new resource was created  as a result
 The response is ent after after `POST` requests or some `PUT` requests

- `202 Accepted`

The request has been received but  not yet acted upon. 


- `203 Non-Authoritative Information`

This response code means the returned metadata is not exactly the same as is available from the origin server, but is collected from a local or a third-party copy

- `204 Reset Content`
There is no content to send  fro this request, but the headers are useful

- `205 Reset Content`

Tells the user to reset the content which sent the request

- `206 Partial Content`