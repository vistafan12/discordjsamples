# Joined user to server
Code:
```javascript
client.on("guildMemberAdd", (member) => {
    console.log(`New user "${member.user.username}" joined to "${member.guild.name}"` );
    member.guild.defaultChannel.sendMessage(`"${member.user.username}" joined to this server!`);
});
```
Your bot should look like this:
```javascript
const Discord = require('discord.js');
const client = new Discord.Client();

client.on("guildMemberAdd", (member) => {
    console.log(`New user "${member.user.username}" joined to "${member.guild.name}"` );
    member.guild.defaultChannel.sendMessage(`**${member.user.username}** has joined to this server!`);
});
client.on('message', message => {
  if (message.content === 'ping') {
    message.reply('pong');
  }
    }
});

client.login('token here');
```
![alt tag](http://i.imgur.com/yiTqjvR.png)
