# Set game status
Code:
```javascript
client.on("ready", () => {
  client.user.setGame("game");
});
```
Your bot should look like this:
```javascript
const Discord = require('discord.js');
const client = new Discord.Client();

client.on("ready", () => {
  client.user.setGame("with my code");
});
client.on('message', message => {
  if (message.content === 'ping') {
    message.reply('pong');
  }
    }
});

client.login('token here');
```
![alt tag](https://puu.sh/v5zgu/bfa16e94a3.png)
