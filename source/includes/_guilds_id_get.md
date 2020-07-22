## GET Guild

```shell
curl "https://unbelievaboat.com/api/v1/guilds/305129477627969547"
  -H "Authorization: API_TOKEN"
```

```javascript
const { Client } = require('unb-api');
const client = new Client('API_TOKEN');

const guildID = '305129477627969547';

client.getGuild(guildID);
```

```python

```

> Response:

```json
{
  "id": "305129477627969547",
  "name": "🍕 UnbelievaBoat 🍕",
  "icon": "a_2cadce0327733c0b1835883eb7fd9660",
  "owner_id": "261674810914897931",
  "member_count": 123456,
  "symbol": "<:applepizza:451430693147508746>"
}
```

`GET /guilds/{guild.id}`

### JSON Response

Field | Type | Description
--------- | ------- | -----------
id              | String    | Guild id
name            | String    | Guild name
icon            | String    | Icon hash
owner_id        | String    | User ID of the owner
member_count    | Number    | Total number of members
symbol          | String    | Currency symbol
