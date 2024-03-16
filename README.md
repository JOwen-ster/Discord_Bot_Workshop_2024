# Discord_Bot_Workshop_2024
A repo on how to setup a discord bot step by step!

![Discord_Python_Logo](https://images.opencollective.com/discordpy/25fb26d/logo/256.png)

### Creating Your Application
Head over to the [discord developer page](https://discord.com/developers/applications), log in, and in the top right click `New Application`.

> [!NOTE]
> For simplicity we will not select a team, but you can create a team in the 'Teams' tab and add people that will be associated with the development of the bot!

Click on the `Bot` tab and then go to `Privileged Gateway Intents`. These are the different types of data that your bot will have access to when in a server. You can read about them by clicking the [links](https://discord.com/developers/docs/topics/gateway#gateway-intents) to see what each intent covers and if you may need a single or multiple when you make your own bot!

> [!NOTE]
> For simplicity, we will use all gateway intents in case you want to add more to your first bot. In real practice, you want to read up on these intents and see which you really do need since when you apply to get your bot verified at 75 servers, discord will ask you why you are using them! You will need to apply for gateway intents separately with the verification process. If you have any questions about verifying a discord bot, ask me ([@JOwen-ster](https://github.com/JOwen-ster) on GitHub or [@typos.](https://discord.com/) on Discord) since I have a bot that is in 200+ servers and is verified!

Next, head over to the `OAuth2` Tab and then in the dropdown menu for `Default Authorization Link`, click on `In-app Authorization`.
* Under Scopes -> click `bot`
* Under Bot Permissions -> click any permissions that you bot will need.

This will make it so people can add your bot from its profile with these selected perms to any server they have the `Manage Server` permission in.

> [!NOTE]
> For this workshop we will use the `Administrator` perm since it will cause no conflict since the bot will have access to all channels with all permissions.
> Bots are treated like regular members/users with their access to channels and ways they interact with the server like being able to manage messages is not a usual default perm for most servers, it is not for a bot unless you give it that perm.

> [!WARNING]
> Unless your Discord bot's function is for server management such as raid protection, server setup, moderation, or various non member interactive things, I would **NOT** set your permissions as Admin just because it is "easy". From my bot developing experience, when getting bots into bigger servers, some owners really wanna limit what it can do for security purposes. As an example, if your token gets exposed, someone logs into your bot and with a total of 20 lines of code (not joking) every server that bot is in, it will nuke, mass ping, and ban every member.

Finally, scroll down till you see `OAuth2 URL Generator`
* Under Scopes -> click `bot`
* Under Bot Permissions -> click any permissions that your bot will need.

This will create a link that people can click to add your bot to any server with these selected perms to any server they have the `Manage Server` permission in.

## Before we get coding...
> [!IMPORTANT]
> Go to the `Bot` tab.
> Click `Reset Token` near the top of the page

***__COPY AND SAVE THIS TOKEN SOMEWHERE SECURE AND SOMEWHERE YOU CAN ACCESS IT__***

> [!CAUTION]
> **THIS TOKEN IS HOW TO CONNECT TO YOUR APPLICATION WITH CODE, NO ONE NEEDS ANYTHING ELSE TO CONNECT/LOG INTO YOUR BOT EXCEPT THE MOST RECENT TOKEN. NEVER POST IT OR YOU RISK YOUR BOT GETTING HIGHJACKED**

> [!CAUTION]
> If you do not gitignore the `.env` file in your `.gitignore` (which is where you put your token, not in your bot code) (and you should use a .env for storing your token in code and a .gitignore to hide private files), then GitHub bots **will** scrape your token (it has happened to me) and may use it. Discord will hopefully send you a message very fast saying they caught it and reset it since they are also scraping for Discord Bot Tokens to watch out for you anid keep your bots secure :)


## Coding the Actual Discord Bot
[Read the docs (Commands)](https://discordpy.readthedocs.io/en/stable/ext/commands/commands.html)
[Read the docs (Events/Listeners)](https://discordpy.readthedocs.io/en/stable/api.html?highlight=event#discord-api-events)

