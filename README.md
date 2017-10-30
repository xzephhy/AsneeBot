## Synopsis

I decided to create a discord bot from scratch, by teaching myself JavaScript, there's a lot I still have to learn about programming as a whole.
However, ever since I've started taking programming as a hobby, this is a project solely based on my own personal development as a programmer.
If you stumble across this page, there are some things you should know.


Currently AsneeBot is being created in JavaScript, using my favourite editor, Atom. 


## Code Example

const Discord = require("discord.js");
const client = new Discord.Client();

client.on("ready", () => {
  console.log("I am ready!");
});

client.on("message", (message) => {
  if (message.content.startsWith("ping")) {
    message.channel.send("pong!");
  } else

  if (message.content.startsWith("foo")) {
    message.channel.send("bar!");
  }
});

client.login("")
