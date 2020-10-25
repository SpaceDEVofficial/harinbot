# Public Commands Sumup
Suggester contains a lot of commands everyone can use, but they don't really need a whole article for each and every of them, as they are mostly basic. You'll find in this page the full list of public commands with a quick explanation of what they do.

Commands in this list will use the default prefix (`.`), meaning if you configured a different one, you will have to replace it accordingly.

### Commands Anyone Can Use

`.help`: Shows an interactive menu containing all Suggester's commands, can also include a command argument (`.help <command>`) to get info about a specific command

`.ping`: Displays the response time and some other information about the bot

`.support`: Sends the link to our [support server](https://discord.gg/G5pEdUp) where you can get in touch with our Support Team

`.invite`: Sends the link to [add the bot](https://discord.com/oauth2/authorize?client_id=564426594144354315&scope=bot&permissions=805694544) to your server

`.vote`: Shows information about voting for Suggester on several bot lists 

`.verify`: Shows a user permissions as they relate to the bot, also accepts a mention/user ID argument to check someone else's permissions

`.prefix`: Shows the current configured prefix in your server

`.changelog`: Links the latest stable release from [GitHub](https://github.com/Suggester/Suggester/releases/latest)

`.tutorial`: Shows a quick guide about setting up and using the bot (the response to this command is the same as the embed sent when the bot is added to a server)

`.github`: Sends a link to Suggester's repository

`.shard`: Tells which shard the current server is on ([What's that?](https://discord.com/developers/docs/topics/gateway#sharding))

## Special Sunflowers

These are special commands everyone can use, so we added them to another part :3

`.notify`: Set your notification settings for the current server, running this command with no argument will show your current settings. To edit them, you'll need an extra argument explained below

| Argument              |                Description                   |
|-----------------------|:--------------------------------------------:|
| `on`                  | Enable notifications                         |
| `off`                 | Disable notifications                        |
| `toggle`              | Toggle the current state                     |
  
`.suggest`: Suggester's main command! Use it to suggest stuff in your favorite servers, you can also add an attachment by attaching it to the command message! 

`.locale`: This command sets your **user** locale, all responses and messages you receive from the bot will use that language (defaulting to English). Using it with no arguments will show a list of all available locales

?> Since translations are community made, all strings might not yet be translated when you'll see them in the bot


## Suggestion Following

### What is that?
You can follow suggestions to be notified when a change is made to them. It works just like normal notifications, but the title refers to "a suggestion you follow" instead of "your suggestion". You can follow suggestions by using the [`.follow`](following/follow.md) command, or upvoting them (you will receive a DM the first time you upvote a suggestion which will contain basic information about following, don't worry we'll explain it below)

### Autofollowing 
By default, you'll automatically follow suggestions you **upvote**, though that can be disabled using `.follow auto off` whic means you will not receive notifications for suggestions you've autofollowed in the past, and you won't follow any more automatically. If you turn it back on, you'll receive notifications again for suggestions you autofollowed. This should respect all server and user notification settings.










