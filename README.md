# ADIB HOQUE API
I searched for motivation images api to use but didn't find one so I motivated myself and made one! 

If you want to use this simple api for your discord bot, generate a number between 1-106 and put it in this format https://raw.githubusercontent.com/AdibHoque/API/master/Motivation/%20{number}.jpg replacing the {number} with number! 

# EXAMPLE 
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
    
@bot.command(ctx)
async def motivation():
    number = random.radiant(1, 106)
    imgurl = 'https://raw.githubusercontent.com/AdibHoque/API/master/Motivation/%20+number'+'.jpg'
    embed = discord.Embed(title = 'Motivation', color = 0xFFBF00)
    embed.set_image(url = imgurl) 
    await bot.say(embed)
    
bot.login('token') 
```
## discord.js
