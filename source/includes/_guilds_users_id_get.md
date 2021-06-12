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
import unbelievaboat
unbclient = unbelievaboat.client('API_TOKEN')
guildid = '305129477627969547'
userid = '261674810914897931'
unbclient.get_user_bal(guildid, userid)
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
rank?       | String    | Leaderboard rank of the user. This is only present on GET User Balance and GET Guild Leaderboard
user_id     | String    | User ID of the discord user.
cash        | Number    | User's cash balance.
bank        | Number    | User's bank balance.
total       | Number    | User's total balance.
