Discord .NET Bot Template

This Template has all you need to get started on creating a bot quickly and easily. Included is a very simple working bot.

To get started, make sure you have Docker installed on whatever OS you're using. For more information, you can go to https://docs.docker.com/get-started/

Once you have Docker, you're ready to run the app! But in order for the bot to actually work, you'll need to set up your Discord Bot here: https://discord.com/developers. If you need help, you can find some instructions here: https://discordnet.dev/guides/getting_started/first-bot.html. Be sure to make note of the Bot token as you'll be using it later.

Once you have set up your bot and have the project pulled down, do the following:
1. Copy the file in the root of this directory called `docker-compose.override.yml.sample`
1. Rename it to `docker-compose.override-yml`. This file will not be checked in!
1. Take the Bot token you pulled out when setting up your Discord Bot. Replace the placeholder token text with your bot string.
1. Add your bot to your Discord server. Info on how to do it is here: https://discordnet.dev/guides/getting_started/first-bot.html
1. Run `docker-compose up` in your favorite terminal at the roo of the project to start up this application. 
1. Run the included `!ping` command in a text channel on your server that the bot as access to. If everything is set up correctly, it should respond.

From here you can write your own commands. There's more than enough here to create a pretty advanced bot, but feel free to check out the documentation for Discord .NET on how to do some of the more advanced stuff.