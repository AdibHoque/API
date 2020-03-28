# ADIB HOQUE API
I searched for motivation images api to use but didn't find one so I motivated myself and made one! 

If you want to use this simple api for your discord bot, generate a number between 1-106 and put it in this format https://raw.githubusercontent.com/AdibHoque/API/master/Motivation/%20{number}.jpg replacing the {number} with number! 

# EXAMPLEs
## discord.py 
```
import discord
from discord.ext import commands
import asyncio 
import random 

bot = commands.Bot(prefix='prefix')

@bot.event()
async def on_ready()
    print('Online')
    
@bot.command(pass_context=True)
async def motivation(ctx):
    number = random.radiant(1, 106)
    imgurl = 'https://raw.githubusercontent.com/AdibHoque/API/master/Motivation/%20'+number+'.jpg'
    embed = discord.Embed(title = 'Motivation', color = 0xFFBF00)
    embed.set_image(url = imgurl) 
    await bot.say(embed)
    
bot.run('token') 
```
## discord.js
```
const {Client , Util , RichEmbed, MessageAttachment, avatarURL} = require('discord.js'); 
const client = new Client({ disableEveryone: true }); 
const random = require('random')
const PREFIX = 'prefix'

client.on('error', console.error);

client.on('ready', () => console.log('Yo this ready!'));

client.on('disconnect', () => console.log('I just disconnected, making sure you know, I will reconnect now...'));

client.on('reconnecting', () => console.log('I am reconnecting now!'));

client.on('message', async msg => { // eslint-disable-line

	if (!msg.content.startsWith(PREFIX)) return undefined;
	const arg = msg.content.split(' ');
	const args = arg.slice(1).join(' ');
        let message = msg
        const everyone = message.guild.roles.find(r => r.name === "@everyone"); 
	let command = msg.content.toLowerCase().split(' ')[0];
	command = command.slice(PREFIX.length)

  if(command === 'motivation') {
  const number = random.int(min = 1, max = 106);
  const imgurl = 'https://raw.githubusercontent.com/AdibHoque/API/master/Motivation/%20'+number+'.jpg'
  const embed = new RichEmbed()
  .setTitle('Motivation') 
  .setImage(imgurl)
  msg.channel.send(embed);
 };
 
client.login('TOKEN')
```
