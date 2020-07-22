## GET Application Permissions

```shell
curl "https://unbelievaboat.com/api/v1/applications/@me/guilds/305129477627969547"
  -H "Authorization: API_TOKEN"
```

```javascript
const { Client } = require('unb-api');
const client = new Client('API_TOKEN');
    
const guildID = '305129477627969547';
    
client.getApplicationPermission(guildID)
    .then(permission => {
        console.log(permission.has('economy'));
    });
```

```python

```

> Response:

```json
{
  "permissions": 1
}
```

`GET /applications/@me/guilds/{guild.id}`

Get an applications permissions for a guild (whether it has been authorized or not).  
You can check a permission using the bitwise AND operator.  
For example: <code>(permissions & 1) == 1</code>  

### Bitwise Permission Flags

Permission | Value | Description
--------- | ------- | -----------
ECONOMY   | 0x00000001    | Access and edit this servers economy

### JSON Response

Field | Type | Description
--------- | ------- | -----------
permission  | Number    | bitwise value of the enabled permissions
