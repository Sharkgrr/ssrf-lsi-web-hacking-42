# How to defend aggainst SSRF & LSI Attacks 

## Sanitization and Validation

As with most vulnerabilities, a pain-point in SSRF attacks is the use of untrusted data. Always treat any data coming from the client side as untrusted.

Example: "validUrlRegex = /^http:\/\/\S+$/;"

## Whitelists

A list of entities that are granted access to a particular system or service.

### Restricted IP 

The idea is that the application has only one administrator and one user with restricted permissions, or a list of IPs that are allowed to access the endpoints.

### Requests (LSI)

Create a list of allowed requests in the fetch, and block any other requests that are not permitted.

