# History Of Http 
## Evolution of http
HTTP (HyperText Transfer Protocol) is the underlying protocol of the World Wide Web. Developed by Tim Berners-Lee and his team between 1989-1991, HTTP has seen many changes, keeping most of the simplicity and further shaping its flexibility. HTTP has evolved from an early protocol to exchange files in a semi-trusted laboratory environment, to the modern maze of the Internet, now carrying images, videos in high resolution and 3D.

In 1989, while he was working at CERN, Tim Berners-Lee wrote a proposal to build a hypertext system over the Internet. Initially calling it the Mesh, it was later renamed to World Wide Web during its implementation in 1990. Built over the existing TCP and IP protocols, it consisted of 4 building blocks:

A textual format to represent hypertext documents, the HyperText Markup Language (HTML).
A simple protocol to exchange these documents, the HypertText Transfer Protocol (HTTP).
A client to display (and accidentally edit) these documents, the first Web browser called WorldWideWeb.
A server to give access to the document, an early version of httpd.

## HTTP/0.9 – The one-line protocol

It was very simple it contained only get method and the file name of the html file.
request - GET /mypage.html
response -<HTML>
A very simple HTML page
</HTML>

## HTTP/1.0 – Building extensibility
Versioning information is now sent within each request (HTTP/1.0 is appended to the GET line)
A status code line is also sent at the beginning of the response, allowing the browser itself to understand the success or failure of the request and to adapt its behavior in consequence (like in updating or using its local cache in a specific way)
The notion of HTTP headers has been introduced, both for the requests and the responses, allowing metadata to be transmitted and making the protocol extremely flexible and extensible.
With the help of the new HTTP headers, the ability to transmit other documents than plain HTML files has been added (thanks to the Content-Type header).

## HTTP/1.1 – The standardized protocol
The first standardized version of HTTP, HTTP/1.1 was published in early 1997, only a few months after HTTP/1.0.
HTTP/1.1 clarified ambiguities and introduced numerous improvements:

A connection can be reused, saving the time to reopen it numerous times to display the resources embedded into the single original document retrieved.
Pipelining has been added, allowing to send a second request before the answer for the first one is fully transmitted, lowering the latency of the communication.
Chunked responses are now also supported.
Additional cache control mechanisms have been introduced.
Content negotiation, including language, encoding, or type, has been introduced, and allows a client and a server to agree on the most adequate content to exchange.
Thanks to the Host header, the ability to host different domains at the same IP address now allows server colocation.

## HTTP/2 – A protocol for greater performance
The HTTP/2 protocol has several prime differences from the HTTP/1.1 version:

It is a binary protocol rather than text. It can no longer be read and created manually. Despite this hurdle, improved optimization techniques can now be implemented.
It is a multiplexed protocol. Parallel requests can be handled over the same connection, removing the order and blocking constraints of the HTTP/1.x protocol.
It compresses headers. As these are often similar among a set of requests, this removes duplication and overhead of data transmitted.
It allows a server to populate data in a client cache, in advance of it being required, through a mechanism called the server push.
