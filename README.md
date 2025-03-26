
import discord
import os
import random
from discord.ext import commands

intents = discord.Intents.default()
intents.message_content = True
bot = commands.Bot(command_prefix='$', intents=intents)

@bot.event
async def on_ready():
    print(f'We have logged in as {bot.user}')

@bot.command()
async def medioambiente(ctx): # type: ignore
    await ctx.send(f'Reducir el consumo de recursos, como plásticos de un solo uso, energía y agua, es uno de los métodos más efectivos. {bot.user}!')

@bot.command()  # Corregido: Se agregaron paréntesis en @bot.command()
async def coches(ctx): # type: ignore
    await ctx.send(f'Es recomendable el uso de transporte público o vehículos eléctricos, y cuando sea posible, ir en bicicleta o caminar. {bot.user}')  # Corregido: `await ctx.send(...)`

bot.run("MTM1NDI0MDM4Mzk0MDI5Njg2NQ.GzHkAI.D-VHDx2BQsx-utrmbENxlR5iUv0igoTOdEDcpI")  # Asegúrate de reemplazar esto con tu token real
