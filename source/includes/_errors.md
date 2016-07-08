# Errors

```json
{
  "error": "Not authorized"
}
```

The unofficial list of HTTP status codes that the API is going to respond with:

Code | Status             | Description
---- | ------             | -----------
200  | Success            | Success
400  | Bad Request        | Request is invalid or request is missing an Authorization header
401  | Unauthorized       | Request is missing an Authorization header or authentication has failed
403  | Forbidden          | User is not authorised to access resource
404  | Not Found          | URI is invalid or resource doesn't exist. Or request format is using the wrong method
422  | Unprocessable Entry| Resource couldn't be created, saved, or deleted


<!-- Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request sucks
401 | Unauthorized -- Your API key is wrong
403 | Forbidden -- The kitten requested is hidden for administrators only
404 | Not Found -- The specified kitten could not be found
405 | Method Not Allowed -- You tried to access a kitten with an invalid method
406 | Not Acceptable -- You requested a format that isn't json
410 | Gone -- The kitten requested has been removed from our servers
418 | I'm a teapot
429 | Too Many Requests -- You're requesting too many kittens! Slow down!
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarially offline for maintanance. Please try again later.
 -->