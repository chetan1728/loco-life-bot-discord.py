import discord
from discord.ext import commands
from discord.ext.commands import Bot
import asyncio

bot = commands.Bot(command_prefix='/')

@bot.event
async def on_ready():
    print ("Ready when you are xd")
    print ("I am running on " + bot.user.name)
    print ("With the ID: " + bot.user.id)

@bot.command(pass_context=True)
async def stock(ctx):
    await bot.say("Lives stock   :loco: 51547")
    print ("stock is available ")

@bot.command(pass_context=True)
async def points(ctx):
	await bot.say("points:1000")
	print("hu")
@bot.command(pass_context=True)
async def loco(ctx):
	await bot.say("generating life for loco ")
	await bot.say("generated life for loco")
	print("hu")
@bot.command(pass_context=True)
async def create(ctx):
	await bot.say("/locolife (amount) (refer code)")
@bot.command(pass_context=True)
async def lf(ctx):
	await bot.say("correct use (/lf (amount) (refer code))")

@bot.command(pass_context=True)
async def info(ctx, user: discord.Member):
    await bot.say("The users name is: {}".format(user.name))
    await bot.say("The users ID is: {}".format(user.id))
    await bot.say("The users status is: {}".format(user.status))
    await bot.say("The users highest role is: {}".format(user.top_role))
    await bot.say("The user joined at: {}".format(user.joined_at))

@bot.command(pass_context=True)
async def kick(ctx, user: discord.Member):
    await bot.say("boot Cya, {}. Ya loser!".format(user.name))
    await bot.kick(user)

@bot.event
async def on_ready():
	print('Logged in as')
	print(bot.user.name + "#" + bot.user.discriminator)
	print(bot.user.id)
	print('------')
	await bot.change_presence(game=discord.Game(name="with locolives/creator CHETAN"))
bot.run('')
