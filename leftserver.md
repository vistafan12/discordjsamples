# Left user in server
Code:
```javascript
client.on("guildMemberRemove", (member) => {
    console.log(`"${member.user.username}" he left the "${member.guild.name}"` );
    member.guild.defaultChannel.sendMessage(`**${member.user.username}** left this server!`);
});
```
Your bot should look like this:
```javascript
const Discord = require('discord.js');
const client = new Discord.Client();

client.on("guildMemberRemove", (member) => {
    console.log(`"${member.user.username}" he left the "${member.guild.name}"` );
    member.guild.defaultChannel.sendMessage(`**${member.user.username}** left this server!`);
});
client.on('message', message => {
  if (message.content === 'ping') {
    message.reply('pong');
  }
    }
});

client.login('token here');
```
![alt tag](http://i.imgur.com/ivOcWcc.png)
