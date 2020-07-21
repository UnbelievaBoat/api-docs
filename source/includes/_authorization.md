## Authorization

```javascript
const { Client } = require('unb-api');
const client = new Client('API_TOKEN');
```

```python

```

```shell
# With curl, you pass the Authorization header with each request
curl "https://unbelievaboat.com/api/" -H "Authorization: API_TOKEN"
```


> Make sure to replace `API_TOKEN` with your API token.

All requests require the <code>Authorization</code> header to be set.  
Authorization type is not required, it's just the token.

### Bot Authorization
API tokens can be created for Discord bots which allows them to make requests on guilds they have been authorized on.

<a href='https://unbelievaboat.com/applications' target="_blank">Get your API Token</a>
