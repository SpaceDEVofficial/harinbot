# Changelog

### Suggester v4.10.1 (May 13th, 2021)
Discord has [rebranded](https://dis.gd/ournewlook), changing their old blurple color (#7289DA) to a new brighter blue (#5865F2). Since Suggester's profile picture and default color scheme used the OG Blurple color, we're rebranding our icons and assets as well. You'll notice a brand new Suggester icon, as well as a new default color for suggestion embeds and some emojis used by the bot. And happy birthday Discord!!

### Suggester v4.9.10 (April 15th, 2021)

**New Things**\
• Commands can now be disabled server-wide using `.config disabledcommands [add/remove] [command name]`\
• Channels can now be disabled, meaning the bot will not respond to any commands in that channel. This is done using `.config disabledchannels [add/remove] [#channel]`\
• The `privacy` command has been added, linking to our privacy policy.

**Improvements**\
• The prefix can now be edited using the `.prefix` command directly. This is done using `.prefix [your new prefix here]`

**Bug Fixes**\
• Blocked users can no longer use `/asuggest`\
• Comments added through the `.mark` command are no longer duplicated

**Removed**\
• The `.stats` command was removed because the information it provided was outdated

### Suggester v4.1.2021 (April 1st, 2021)
Suggester v4.1.2021 is the largest overhaul Suggester has ever had. We coded until our fingers couldn't anymore, and then we started using our toes. This update contains major updates to our patented SuggestionCreator3000™, allowing for even better-er suggestion creation. The bot also now runs 0% faster, and uses 500% more memory (meaning it will remember your suggestions better... yay!) 

...and it now has owo mode
thank you for your time and have a good day

If you hate owo mode you can use `.locale eng` to go back to English but everyone will judge you for it! 

---
### Suggester v4.9.1 (March 29th, 2021)
- The live vote count on suggestions can now be hidden using `config votecount off`
- When the `autoapprove` mode is set, the response to the `deny` command will now mention the `delete` command
- The bot now responds with the prefix if the message is just the bot mention
- If a server is set as a Community on Discord and has a locale set in Server Settings, the bot will try to find that locale and set it as the configured locale on the bot 

---
### Suggester v4.9 (March 23rd, 2021)
🆕 **New Things**
- Added the `shards` command to show information about all bot shards
- Added the `search` command, which takes an unlimited number of query parameters, space-separated to query all suggestions on the server. See this [page](topics/search.md) for more information.

🔧 **Improvements**
- The emojis used in the `mark` command are now colorblind-friendly
- You can now add attachments to suggestions awaiting review through the `attach` command
- The `info` command now shows a timestamp for when the suggestion was submitted
- There is now an error message shown when trying to set the `cooldown` config element lower than the global cooldown for the `suggest` command
- The denial reason is now shown in the review message when "A change has been processed on this suggestion" is shown
- The `setup` command now links to the documentation for each config element
- Using `default` as the emoji setting will restore a reaction to its default configuration
- `dupe` can now be used on approved suggestions, deleting them from the suggestions feed

🐛  **Bug Fixes**
- The `help` command is no longer available in DMs
- Anonymous suggestions now properly handle allowed roles configuration and checking
- Anonymous suggestions will now show as anonymous in the denied suggestions feed
- Missing upvote/downvote reactions should no longer cause issue with live vote totals and `colorchange` config

---
### Suggester v4.7.2 (January 31st, 2021)
- The `ping` command has been redesigned to show more information and not error when the bot is starting up
- The `mark` command should no longer output an error if you don't specify a status in the command and select a reaction to choose one
- Voting totals (upvotes/downvotes) should be more accurate now
- **@everyone** and **@here** mentions for the `feedping` and `reviewping` elements now resolve correctly and ping intended users


---
### Suggester v4.7.1 (January 6th, 2021)
- We now support importing suggestions from the `Gaius Cicereius#3705` bot
- You can now enable/disable comment timestamps on the suggestion embeds using `cfg commenttime [on/off/toggle]` 

---
### Suggester v4.7 (January 4th, 2021)
- This release brings a new major feature to the bot: a Trello integration! We have a new documentation page for it, which can be found [here](/topics/trello/intro.md), and you can also use `config help trello` to find more examples
- The `queue` command now shows the suggestions you are viewing out of the whole in the title (ex. 1-10 out of 20)
- `shortinfo` now has options to shorten the output:\
Adding `-trimsuggest` (or `-ts` for short) to the end will limit the suggestion content output to 250 character\
Adding `-noattach` (`-na` for short) will hide the suggestion's attachment
- Added suggestion caps: these prevent more suggestions from being submitted if the number of approved, non-denied, non-implemented suggestions is greater than or equal to the amount configured using `config cap`
- Command-specific documentation links can now be found in `help [command]`, as well as in `config help [element]`
- Added the feed ping role: when a suggestion is sent to the suggestions feed via autoapprove or manual approval the role will be mentioned. This role can be configured using `config feedping`. Due to there now being 2 ping roles, the old `pingrole` is now called `reviewping`
- Messages from blocked users are now deleted when `inchannelsuggestions` is enabled
- `autosetup` channel names now reflect guild locale-specific configuration
- Servers with over 5000 members may receive a large server protip
- `in` was removed as an alias for  the "in progress" status
- Global cooldown messages will now be affected by server `cleancommands` configuration
- Minor bugfixes and improvements

<!-- tab:2020 -->

---
### Suggester v4.6.1 (December 14th, 2020)
- Added a comment editing feature for server staff! You can now use `editcomment [comment ID] [new content]` to modify comments either posted by you or posted anonymously
- Fixed a bug where suggestions couldn't be deleted if their review channel had been deleted
- Added the "Read Message History" permission to some commands where the bot adds reactions
- Re-implemented and improved a legume-themed easter egg from a long time ago.. (we did it! 🎉)

---
### Suggester v4.6 (November 20th, 2020)
- The ability to edit suggestions has been added! Users can now edit suggestions they’ve submitted, and server admins/staff can edit any suggestion (the footer will show if the suggestion was edited by a staff member). A user editing their own approved suggestion in the review mode will send the edit for review
- Added a `shortinfo` command for when you want to show info about a suggestion in a concise manner without any internal information like the staff member who took action on it
- Added an implemented suggestion role (`cfg implementedrole`), so users who get their suggestions marked as Implemented can receive a role
- Added a configuration element to control auto-following server-wide (`cfg autofollow`) which is enabled by default
- The `top` command is now numbered 
- Server staff/admins are now exempted from the configured suggestion cooldown
- The character limit on suggestions has been raised to 1900 characters (previously 1024)
- The comment limit is now 15 comments per suggestion

**5000**: Thanks for helping Suggester reach 5000 Servers! To celebrate, we'll be giving out 10 VoteBoat votes to 5 winners in a giveaway on our [Support Server](https://suggester.js.org/support)! 

---
### Suggester v4.5.1 (October 21st, 2020)

This release primarily contains performance improvements for servers with a large number of approved suggestions/members who vote on suggestions:
- The `top` & `down` commands now use cached votes, which should considerably improve the time those commands take
- Changed notifications so that logging occurs first, which should reduce lag when a suggestion has a lot of followers
- Fixed a small issue with the `delete` command not working when the suggestion channel was changed
 
---
### Suggester v4.5 (October 17th, 2020)
It’s been a while since we released an update, but we’ve finally got some new stuff for you!

**New Features & Improvements**
- The `cleancommands` config element now applies to more commands. This was mainly applied to commands that are used frequently or where the response is mostly just to let you know the command succeeded. Both the command message and the bot response are deleted after 7.5 seconds.
- We’ve added a new suggestion cooldown (`config cooldown`) config element! After submitting a suggestion, users must wait the configured duration before submitting another. Server staff members can waive this cooldown using the `exempt` command.
- The `dupe` command has been added so that you can deny a suggestion as a duplicate of another. Usage is `dupe 1 2` (1 being the duplicate suggestion and 2 being the original)
- Removed the “You already have a suggestion awaiting review” message due to overall negative feedback
- `prefix` is now its own separate command
- 👻 

**Bug Fixes**
- Fixed handling of the commands channel for servers who had one set before the 4.4 release
- System messages are no longer accepted for `inchannelsuggestions`
- Reactions are now removed from the review message when using massapprove/deny
- Other minor things

---
### Suggester v4.4 (September 18th, 2020)
- You can now __follow__ suggestions to be notified when they are updated. This works just like notifications sent to the suggester, but you can get them for suggestions you didn't submit. You can follow suggestions using the `follow` command and by upvoting any suggestion!
- Users can now be blocked from using the bot for a period of time using `block [user] [time]`
- You can now set multiple commands channels using `config commands add #channel`
- The `top` command now accepts a time argument, which filters the results for suggestions submitted only within the specified time
- The `down` command has been created, so now you can see a list of which suggestions your members don't like (this accepts a time argument too!)
- Attachments are now stored in a manner that allows `cleancommands` to work without the image not resolving 
- If you change the suggestions channel you should still be able to interact with suggestions that are in the old channel
- There is no longer a redundant reply message when you react to approve/deny
- The `github` command shows the link to Suggester's GitHub repository
 
We also added a new **large server** system. If your server has a large (as in several thousands) number of members or high volume of suggestions and would benefit from features like an increased `top` command view and reduced cooldowns for server staff members, contact our [Support Team](https://suggester.js.org/support) and we'll work from there.

---
### Suggester v4.2.2 (September 2nd, 2020)
- `config help notify` now shows correct information
- Translations are now shown properly in `config help`
- The tutorial message no longer shows a random string at the bottom
- The number of suggestions in the playing status will now update 
- "MB" is no longer repeated in the `ping` command 
- Added some memory reduction processes
- The average uptime value is no longer 0

---
### Suggester v4.2.1 (August 12nd, 2020)
- The help command has been reworked to give a list of commands inside Discord, instead of using an external documentation site. Additionally, using `help [command]` now shows examples on how to use most commands.
- Using `config help` will show information about using the config command and configuring all elements of the bot
- The `locales` embed has been redesigned to separate locales that are incomplete and mostly complete
- Redesigned the `ping` and `verify` commands
- Minor bugfixes and improvements

Additionally, with school and things ramping up around this time we might not have as much time to push new features. To help us prioritize features you want added, vote on your favorites in the [support server](https://suggester.js.org/support)!

---
### Suggester v4.2 (August 4th, 2020)
- We've added an `import` command that allows you to import old suggestions into the bot. Any messages from users are imported as their suggestions, and we also support importing suggestions from the bots listed [here](admin/import.md#supported-bots)
- You can now view the top 10 list of highest voted suggestions in your server using the `top` command!
- Suggester now has protips, which give you some helpful tips about using the bot every so often. If you're already a pro, you can disable these using the `protips` command 😎
- Live vote totals are now shown on suggestions
- If a suggestion is marked as Not Happening and there is no denied suggestions channel, reactions will be removed

---
### Suggester v4.1.2 (July 20th, 2020) 
- In-channel suggestions are now **disabled** by default, and can be configured using config `sendinchannel <on|off|toggle>`. The release of this feature didn't go as planned, sorry for the confusion it caused.
- A new status has been added: "In Consideration"! Use `mark <suggestion ID> considered` to try it out
- `silentdeny` should now remove reactions from the review embed

---
### Suggester v4.1.1 (July 14th, 2020)
This release contains bugfixes from the v4.1 release from earlier today, specifically:
- Fixed an issue where the some of the presences shown had incorrect information
- The message-in-suggestion-channel suggestion method has been changed so that commands that start with a backslash (\), the server prefix, or the bot's mention (@Suggester) will not submit a suggestion.

---
### Suggester v4.1 (July 14th, 2020)
**New:**
- Suggestions submitted for review (after this release) can now be approved/denied with check and x reactions that are automatically added to the "Suggestion Awaiting Review" embed. The approve/deny commands still exist unchanged.
- You can now configure a list of roles allowed to vote on suggestions in the suggestions feed using `config voting add <role>`. If at least one voting role is configured, reactions from users without any of those roles will be removed.
- Messages sent in the suggestions channel will now be automatically converted to suggestions.
- `config selfvote <on/off>` will enable/disable allowing the suggesting user to vote on their own suggestions (by default users can vote on their own suggestions)
- `config onevote <on/off>` will enable/disable restricting users to picking one reaction option (this option is enabled by default)
- This update brings back a feature we had a long time ago where at a number of upvotes the embed color would change. By default, 15 upvotes will cause the suggestion embed to change to a gold color. This can be configured using `config colorchange color <color>` and `config colorchange number <threshold>`. (If a status is marked on the suggestion, it will take priority over the color change)

**Improvements:**
- Paginated configuration list
- The bot now cycles through a list of statuses
- The help command shows more useful links
- The bot can now be used via DMs for a few commands including `help`, `changelog`, and `ping`
- All discordapp.com links now refer to discord.com

**Bug Fixes/Other:**
- The `deletecomment` command no longer outputs two log messages
- If a pagination embed has less than one page, instructions for navigating via reactions are no longer shown
- The temporary `blacklist` command from the last release was removed
- Fixed a bug where if suggestion was submitted with a newline after the command the first word of the suggestion was sometimes cut out

---
### Suggester v4.0.2 (June 25th, 2020)
- Over the past few weeks, protesters around the world have spoken out against all forms of racism and to proudly declare that Black Lives Matter. Here at Suggester, we support the Black Lives Matter movement and the protests, therefore we are working to eliminate even subtle forms of racism by moving away from terms like “blacklist” and “whitelist”. We have renamed the `blacklist` and `unblacklist` commands to `block` and `unblock`, respectively. This [article](https://9to5google.com/2020/06/12/google-android-chrome-blacklist-blocklist-more-inclusive/) provides more context about why many tech companies are moving away from these terms.
- Fixed the small bug where the text in the footer of the changelog was ordered wrong
- Added `accept` as an alias for `approve`
- Locales are now managed more effectively and are easier to import into the bot without a reboot

---
### Suggester v4.0.1 (June 10th, 2020)
This release contains bugfixes for the v4 release from a few days ago:
- When a suggestion is approved the user now receives the correct link to the suggestion feed message (previously the link ended with /undefined)
- Fixed incorrect locales displaying for staff commands 
- Fixed a bug with logging commands where the date was incorrect (we have some cool charts relating to this, check them out [here](topics/stats.md)
Also we've reached 30,000 suggestions 

---
### Suggester v4 (June 7th, 2020)
For this update, we reworked the entire bot to make some major changes:

**Translations**
Suggester is now available in multiple languages 
There are two different ways to set the language you receive responses in:
- You can set a locale that is specific to yourself using the `locale` command. This setting will apply across all servers you use the bot in.
- Server admins can configure a locale using the `config` command that applies to the entire server. (Note: user-set locales take priority over server-set locales)

Special thanks to all of our translators who helped translate the bot, and canary testers who helped test the new version. 

**Blocked Roles**: Server admins can configure a list of roles that disallow members from using the bot on their server. These roles act just like if you blocked the user with the `block` command.

**Silentdeny/delete**: Silentdeny has been updated so that it no longer DMs the suggesting user. A new `silentdelete` command has been added that deletes a suggestion without DMing the suggesting user or posting to the denied suggestions feed.

**Delete Vote Totals**: Vote totals are now shown in the denied suggestions channel when a suggestion is deleted.

**Configuration Warnings**:
- A prefix containing "suggest" in the setup command will show a warning to reduce the chance of accidentally setting the prefix to .suggest
- Setting the everyone role as a staff or admin role will also show a warning to prevent giving dangerous permissions to all members of the server

**Submitted Suggestion Mentions**:
You can now set a role that is mentioned when a suggestion is submitted for review. This requires the bot to have the Mention Everyone permission

**Statuses with Comments**:
You can now add a comment to a suggestion while you mark a status on it

**Sharding**:
Suggester is now sharded, allowing us to scale past 2,500 servers. Shard information is now shown in the ping command, and you can easily check the shard of your server using the `shard` command.

**Tutorial**:
The message Suggester sends when it joins a server can now be shown at any time using the `tutorial` command.

**Selfnotify**:
The old selfnotify feature that toggled DM notifications when you took action on one of your own suggestions has been removed due to it not being used

---
### Suggester v3.2.4 (June 1st, 2020)
Small hotfix only pushed to Suggester and not on GitHub which allows the bot to be used in news channels

---
### Suggester v3.2.3 (May 21st, 2020)
This release is only being pushed to the main Suggester bot, and will not be shown on GitHub
- This update brings sharding to the bot, as we're getting close to the 2,500 server threshold where the bot must be sharded
- You should not see any differences in how the bot functions, except that the ping command looks different and the stats command has been temporarily disabled

---
### Suggester v3.2.2 (April 24th, 2020)
This release contains bugfixes and minor improvements:
- Timestamps for when suggestions were submitted should be more accurate 
- Fixed an issue with invalid user arguments sometimes not causing commands to stop executing.
- Removed some unused packages and bumped a few to the latest version.

---
### Suggester v3.1.2 (April 23th, 2020)
**New Stuff**
- The new `changelog` command shows the latest released changelog of the bot (with pagination if it's super long)
- `listqueue` is now paginated and each page is limited to 10 suggestions to make things look cleaner

**Fixes**
- When allowed roles are listed on the `suggest` command, no roles get listed twice anymore
- If `cleancommands` is enabled, all suggest commands/responses are now deleted - even if there's an error. (configuration errors aren't removed)
- Updated the bot invite link 

---
### Suggester v3.2 (April 16th, 2020)
We went through #suggestions and asked in #feedback what you wanted to see added to the bot, and then added a massive number of new features! This update also makes the bot more scalable and depending less on the main server.

**Join Message**: When you add Suggester to a server it will now post a message with helpful information about how to use the bot, as well as a link to this server for support.

**Autosetup Command**: Just added Suggester? You can now use .autosetup for the bot to set up a category for itself and configure channels with appropriate permissions!

**Mention Prefix**: You can now trigger any command with a mention prefix

**Comment Dates**: Comments now have GMT dates on them so they're easier to keep track of! Only comments submitted after this announcement will have dates (we didn't track them before)

**Clean Suggestion Commands**: The new `cleancommands` config element allows you to enable suggestion commands and the bot's response being deleted after a few seconds (disabled by default)

**Allowed Roles**: You can now configure roles that are allowed to submit suggestions, which prevents members without those roles from submitting suggestions. Staff and admin roles can also submit suggestions.

**Suggestion Command Channel**: You can now configure a channel that the suggest command can be used in. This prevents it from being used in any other channels.

**Implemented Archive Channel**: Setting an implemented archive channel allows suggestions marked as Implemented using the `mark` command to be moved out of the suggestion feed Once they're in that channel, no further action can be taken on them.

**Near-Matching Strings**: You can now use near-matching strings in configuration instead of the full name. 

**Vote Command Remake**: `.vote` is now much more detailed 

**Cooldowns**: Commands now have cooldowns, preventing excessive spam. Fair warning, you may be blocked from the bot if you violate these cooldowns too many times.

**Verify Changes**: The `.verify` command no longer uses roles from the support server. OG Partners/Contributors/Canary Testers can request a custom acknowledgement by asking a staff member.

**Permissions**: 
- The `help` command will now retrieve information about any command regardless of permissions.
- Suggester no longer reacts with 🚫 if you do not have enough permissions to use a command.

That's a lot of stuff ⚡

---
### Suggester B.E.A.N Edition (April 1st, 2020)
- Everything is bean colored
- Everyone can now use the `bean` command in any server

In other news... If you're trying to create a server and you want basic suggestion channels, feel free to use our template. This template will create a server with the channels/roles you need, and some channels with setup instructions!
https://discord.new/Ye9n7V9SVNPg

---
### Suggester 3.1.4 (March 25th, 2020) 
Due to some issues with configuration changes, some log channels were incorrectly configured and therefore did not function as intended. Any log channel configured while Suggester was on version 2 has now been reset.

**Changelog**
- Use `notify self <on|off|toggle>` to toggle whether or not you receive notifications when you perform an action on your own suggestion.
- Blocking now supports reasons (added to the log channel if one is configured)
- The `help` command now shows the prefix when used
- Using "@Suggester help" now shows a warning when the server is not fully configured with core elements (roles, suggestions channel, review channel if on review mode)
- A few bug fixes : 
**Other Notable Things**
- VoteBoat streaks now work properly, go get those extra votes!
- #feedback was added to the support server to more effectively gather feedback about certain topics. 

---
### Suggester 3.1.2 (March 24th, 2020) 
- Lots and lots of bugfixes
- Removed "shared servers" from `stats` because it didn't work properly anymore and making it work would make the command even more resource intensive

---
### Suggester 3.1.1 (March 23rd, 2020)
- Fixes to lower memory usage
- Fixes for other things

---
### Suggester v3.1 (March 18th, 2020)

**New Stuff**
- Suggester now uses discord.js v12, giving us access to the latest & greatest features
- You can now disable reaction emojis using `cfg emojis <up|mid|down> disable`
- Added some new acknowledgements and emotes to the verify command 😎
- You can now submit attachments with suggestions, simply by attaching a file with your suggestion message! Suggestions can now have content and an attachment, or just either one.
- The new `notify` command allows you to configure whether you (on a user level) get notified for suggestion actions

**Other Stuff**
- Results from mass commands (`mapprove`, `mdeny` and `mdelete`) aren't buggy now
- Minor improvements to speed of some commands
- Emojis now fall back to the default if the configured emoji can't be found
- Fixed a lot of bugs

---
### Suggester v3.0.4 (February 5th, 2020)
The server name is now shown in DM messages about actions


---
### Suggester v2.1 (November 16th, 2019)
This update brings a lot of cool changes, some of which were suggested by yall! 

- **Setup**: Running the `setup` command will initiate a walkthrough for configuring your server, making it much easier than the config command (which still exists)

- **Permission Checks**: The bot now checks permissions in channels before performing actions, making sure everything works as intended

- **Log Channels**: You can now set a log channel where all actions on suggestions are logged using `.config logs #channel`

- **Removing log and denied suggestions channels**: Specifying `none` as the channel in the `config` command will remove the log or denied suggestions channels 

- **Approve, but with comments**: You can now run `.approve` and specify a comment to add to the suggestion!

- **Attach with uploaded attachments**: You can now upload an attachment straight to Discord for the `attach` command and it will be added to the suggestion

- **Mass approve/deny/delete**: You can now approve/deny/delete multiple suggestions at a time using the `mapprove`, `mdeny`, and `mdelete` commands

- **Enable/disable reactions on the suggestion feed**: You can now toggle whether you would like suggestion feed posts to have reactions with `.config emojis toggle`

- **Enable/disable DMs to server members when suggestions are updated**: Using `.config notifications toggle` will toggle whether server members receive DMs when their suggestions are updated

- **Bug fixes**: Gotta catch 'em all!

 
