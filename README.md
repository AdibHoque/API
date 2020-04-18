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
    number = random.randint(1, 106)
    imgurl = f"https://raw.githubusercontent.com/AdibHoque/API/master/Motivation/%20{number}.jpg"
    embed = discord.Embed(title = 'Motivation', color = 0xFFBF00)
    embed.set_image(url = imgurl)
    embed.set_footer(text = 'GitHub.com/AdibHoque/API')
    await bot.say(embed=embed)
    
bot.run('token') 
```
## discord.js
```
const { Client, MessageEmbed } = require('discord.js'); 
const client = new Client();
const PREFIX = 'prefix'

client.on('ready', () => console.log('Online!'));

client.on('message', message => {
  if(command === PREFIX+'motivation') {
  const imgurl = 'https://raw.githubusercontent.com/AdibHoque/API/master/Motivation/%20${Math.floor(Math.random() * 106) + 1}.jpg`
  const embed = new MessageEmbed()
  .setTitle('Motivation') 
  .setImage(imgurl)
  .setFooter('GitHub.com/AdibHoque/API')
  msg.channel.send(embed);
 };
 
client.login('TOKEN')
```
