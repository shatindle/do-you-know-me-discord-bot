# do-you-know-me-discord-bot
A bot to interview new joiners and decide what roles they should get

## Setting up the bot
You will need at least Node.js v16.9.0 to run this bot.

### Steps
Clone the source code, then add a file called .env with the following and fill out the variables with the appropriate values:
```
TOKEN=your discord bot token
GUILD_ID=your server ID
PRIVATE_CHAT=your approval chat ID
GUEST_ROLE=the guest role to assign users who interact with the first buttons
WELCOME_CHAT=the chat users first see that will contain the welcome Guest/I know you buttons
HIGHEST_ROLE=the highest role ID you want to assign users in your role list
LOWEST_ROLE=the lowest role ID you want to assign users in your role list, note that you can pick roles between highest and lowest (inclusive)
```

Create a bot on [discord.com](https://discord.com/developers/applications) and invite it to your server with the following permissions:
- Manage Roles
- Send Messages
- Embed Links

Once the bot is setup and added to your server:
- Run `npm install`
- Run `node ./setup.js` one time to create the welcome modal
- Run the bot via `node ./index.js` or via your favorite process manager

The bot will then interact with your users and interview them.  You can decide to grant higher permissions to anyone you recognize.  All interview responses start with a red border.  They will change to green if you approve them and black if you deny them.