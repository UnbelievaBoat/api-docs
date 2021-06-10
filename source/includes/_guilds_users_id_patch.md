## PATCH User Balance

```shell
curl "https://unbelievaboat.com/api/v1/guilds/305129477627969547/users/261674810914897931"
  -d '{ "cash": -10, "bank": 50 }'
  -X PATCH
  -H 'Accept: application/json'
  -H "Authorization: API_TOKEN"
```

```javascript
const { Client } = require('unb-api');
const client = new Client('API_TOKEN');

const guildID = '305129477627969547';
const userID = '261674810914897931';

client.editUserBalance(guildID, userID, { cash: -10, bank: 50 });
```

```python

```

> Response:

```json
{ 
  "user_id": "261674810914897931", 
  "cash": 190, 
  "bank": 50, 
  "total": 240 
}
```

`PATCH /guilds/{guild.id}/users/{user.id}`

Increase or decrease the User's balance by a value given in the params.  
To decrease the balance, provide a negative number.  
Infinity should be sent as a String instead of a Number.

### JSON Parameters

Field | Type | Description
--------- | ------- | -----------
cash?       | Number    | Value to set the cash balance to.
bank?       | Number    | Value to set the bank balance to.
reason?     | String    | Audit log reason.


Returns the updated User object. 
