## Rate Limits

For every API request made, we return optional HTTP response headers containing the rate limit encountered during your request.

> Header Examples:

```text
X-RateLimit-Limit: 5
X-RateLimit-Remaining: 4
X-RateLimit-Reset: 1595368487253 
```

### Header Format

Header    | Description
--------- | -----------
X-RateLimit-Limit       | The number of requests that can be made.
X-RateLimit-Remaining   | The number of remaining requests that can be made.
X-RateLimit-Reset	    | Epoch timestamp (in milliseconds) at which the rate limit resets.

> 429 Response Example:

```json
{
  "message": "You are being rate limited.",
  "retry_after": 4329
}
```

### 429 Response Fields

Field    | Description
--------- | -----------
message       | You are being rate limited.
retry_after   | The number of milliseconds to wait before submitting another request.

If you exceed the rate limit for the API you will receive an HTTP 429 response code with a JSON body.


> Global 429 Response Example:

```json
{
  "message": "You are being rate limited.",
  "global": true
}
```

### Global 429 Response Fields

Field    | Description
--------- | -----------
message     | You are being rate limited.
global      | A value indicating if you are being globally rate limited.

Additionally, there is a global rate limit of 20 requests per second.
If you exceed this rate limit you will receive an HTTP 429 response code with a JSON body.
