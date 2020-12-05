## GET Guild Leaderboard

```shell
curl "https://unbelievaboat.com/api/v1/guilds/305129477627969547/users?sort=cash"
  -H "Authorization: API_TOKEN"
```

```javascript
const { Client } = require('unb-api');
const client = new Client('API_TOKEN');

const guildID = '305129477627969547';

client.getGuildLeaderboard(guildID, { sort: 'cash' });
```

```python
import unbelievaboat
unbclient = unbelievaboat.client('API_TOKEN')
guildid = '305129477627969547'
unbclient.get_leaderboard(guildid, sort="cash")
```

> Response:

```json
[
  { 
    "rank": "1", 
    "user_id": "198736292039753728", 
    "cash": 54, 
    "bank": 101290610, 
    "total": 101290664 
  },
  {
    "rank": "2", 
    "user_id": "261674810914897931", 
    "cash": 95, 
    "bank": 95044735, 
    "total": 95044830
  }
]
```

`GET /guilds/{guild.id}/users`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
sort?     | total   | Sort the leaderboard by <code>cash</code>, <code>bank</code> or <code>total</code>.
limit?    | null or 1000    | Limit the number of users returned. If page is given the default will be 1000.
offset?   | 1       | Specify the offset of the first user.
page?     | null    | Specify the page. If a page is given, the response will be <code>{ users: Array, total_pages: Number }</code>
