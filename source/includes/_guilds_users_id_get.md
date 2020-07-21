## GET User Balance

```shell
curl "https://unbelievaboat.com/api/v1/guilds/305129477627969547/users/261674810914897931"
  -H "Authorization: API_TOKEN"
```

```javascript
const { Client } = require('unb-api');
const client = new Client('API_TOKEN');

const guildID = '305129477627969547';
const userID = '261674810914897931';

client.getUserBalance(guildID, userID);
```

```python

```

> Response:

```json
{
  "rank": "2",
  "user_id": "261674810914897931",
  "cash": 95,
  "bank": 95044935,
  "total": 95045030
}
```

`GET /guilds/{guild.id}/users/{user.id}`

### Response Fields

Field | Type | Description
--------- | ------- | -----------
rank?       | String    | User ID of the Discord user.
user_id     | String    | Limit the number of users returned. If page is given the default will be 1000.
cash        | Number    | User's cash balance.
bank        | Number    | User's bank balance.
total       | Number    | User's total balance.
