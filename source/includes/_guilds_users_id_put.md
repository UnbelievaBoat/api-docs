## PUT User Balance

```shell
curl "https://unbelievaboat.com/api/v1/guilds/305129477627969547/users/261674810914897931"
  -d '{ cash: 200, bank: 0 }'
  -X PUT
  -H 'Accept: application/json'
  -H "Authorization: API_TOKEN"
```

```javascript
const { Client } = require('unb-api');
const client = new Client('API_TOKEN');

const guildID = '305129477627969547';
const userID = '261674810914897931';

client.setUserBalance(guildID, userID, { cash: 200, bank: 0 });
```

```python
import unbelievaboat
unbclient = unbelievaboat.client('API_TOKEN')
guildid = '305129477627969547'
userid = '261674810914897931'
unbclient.set_user_bal(guildid, userid, cash=200)
```

> Response:

```json
{ 
  "user_id": "261674810914897931", 
  "cash": 200, 
  "bank": 0, 
  "total": 200 
}
```

`PUT /guilds/{guild.id}/users/{user.id}`

Set the User's balance to the given params.  
Infinity should be sent as a String instead of a Number.

### JSON Parameters

Field | Type | Description
--------- | ------- | -----------
cash?       | Number    | Value to set the cash balance to.
bank?       | Number    | Value to set the bank balance to.
reason?     | String    | Audit log reason.


Returns the updated User object. 
