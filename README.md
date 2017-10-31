## Synopsis

I decided to create a discord bot from scratch, by teaching myself JavaScript, there's a lot I still have to learn about programming as a whole.
However, ever since I've started taking programming as a hobby, this is a project solely based on my own personal development as a programmer.
If you stumble across this page, there are some things you should know.


Currently AsneeBot is being created in JavaScript, using my favourite editor, Atom. 


## Code Example
```js
const Discord = require("discord.js");
const client = new Discord.Client();
const config = require("./config.json");


// Set the prefix
let prefix = "-";
client.on("message", (message) => {
  // Exit and stop if the prefix is not there or if user is a bot
  if (!message.content.startsWith(config.prefix) || message.author.bot) return;

  if (message.content.startsWith(config.prefix + "ping")) {
    message.channel.send("pong!");
  } else
  if (message.content.startsWith(config.prefix + "foo")) {
    message.channel.send("bar!");
  }
});

client.login(config.token);
