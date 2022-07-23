[npm](https://www.npmjs.com/package/cors)

[overview](http://en.wikipedia.org/wiki/Cross-origin_resource_sharing)

[baeldung](https://www.baeldung.com/cs/cors-preflight-requests)

In the Same Origin Policy (SOP) context, we consider two URLs to be of the same origin if they have the same scheme, domain and port.

The Same Origin Policy was put in place as the first line of defense to protect against [cross-site request forgery](https://owasp.org/www-community/attacks/csrf) attacks.

The CORS policy defines specific HTTP headers that need to be included in the request/response interaction;

**Any request which is not a simple request is considered a non-simple or a preflighted request.** The browser treats these kinds of requests a little differently. Before sending the actual request, the browser will send what we call a preflight request, to check with the server if it allows this type of request. A preflight request is an OPTIONS request which includes the following headers:

-   _origin_ – tells the server the origin where the request is coming from
-   _access-control-request-method_ – tells the server which HTTP method the request implements
-   _access-control-request-headers_ – tells the server which headers the request includes

Response

```
Access-Control-Allow-Origin: http://yourdomain.com
Access-Control-Allow-Methods: GET, POST
Access-Control-Allow-Headers: X-Custom-Header
```

[Security](Security)

