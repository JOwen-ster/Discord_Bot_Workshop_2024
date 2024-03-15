# Discord_Bot_Workshop_2024
A repo on how to setup a discord bot step by step!

![Discord_Python_Logo](https://images.opencollective.com/discordpy/25fb26d/logo/256.png)

### Creating Your Application
Head over to the [discord developer page](https://discord.com/developers/applications), log in, and in the top right click `New Application`.

> [!NOTE]
> For simplicity we will not select a team, but you can create a team in the 'Teams' tab and add people that will be associated with the development of the bot!

Click on the 'Bot' tab and then can check the 'Gateway' intents. These are the different types of data that your bot will have access to when in a server. You can read about them by clicking the [links](https://discord.com/developers/docs/topics/gateway#gateway-intents) to see which each intent covers and if you may need them when you make your own bot!

> [!NOTE]
> For simplicity, we will use all gateway intenets in case you want to add to your first bot. In real practice, you want to read up on these intents and see which you really do need since when you apply to get your bot verified at 75 servers, discord will ask you why you are using them! You will need to apply for gateway intents separatly with the verification process. If you have any questions about verifying a discord bot, ask me since I have a bot that is in 200+ servers and is verified!

Next, head over to the `OAuth2` Tab and then in the dropdown menu for `Deafult Authorization Link`, click on `In-app Authorization`.
* Under Scopes -> click `bot`
* Under Bot Permissions -> click any permissions that you bot will need.

This will make it so people can add your bot from its profile with these selected perms to any server they have the `Manage Server` permission in.

> [!NOTE]
> For this workshop we will use the `Administrator` perm since it will cause no conflict since the bot will have access to all channels with all permissions.

Finally, scroll down till you see `OAuth2 URL Generator`
* Under Scopes -> click `bot`
* Under Bot Permissions -> click any permissions that you bot will need.

This will create a link that people can click to add your bot to any server with these selected perms to any server they have the `Manage Server` permission in.
