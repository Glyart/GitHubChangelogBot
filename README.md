# GitHubChangelogBot
Simple GitHub changelog bot with some cool features such as:
* 🌐 Multi-language support! You can contribute adding your language, just make a PR!
* ⚙ Extensively configurable, you can tweak basically anything you'll ever need.
* 🍕 Powered by pizza.

## How to install

### Requirements:
* NodeJS (LTS)
* NPM
* A telegram bot token, easily obtained using [Telegram's Bot Father](https://t.me/BotFather).
* A GitHub repository with a valid webhook configuration in order to reach the webserver.
* Some pizza 🍕

### Installation & Configuration:

Having all those requirements met, you just have to install and briefly configure the bot. Let me walk you through this process.

First of all you should clone the repository, after that `cd` into it and run `npm install` in order to download all the needed dependencies for it to run. Then you have to configure the configuration file (config.json).

These are all the settings explained: 

Property | Type | Description
---------|------|------------
**WebServer**||WebServer configuration
shouldCloseOnError|Boolean|Whether the webserver should close on error when starting up or staying online. This is totally up to you. `Default: true`
webhookEndpoint|String|The endpoint which github will be sending requests to. `Example: http://<your-ip>/webhookEndpoint` `Default: /github`
port|Number|The port number which the webserver will be listening to
logging|Boolean|Whether the webserver should be logging requests or not.
**Bot**||Bot configuration
token|String|The telegram's bot token
groupID|Number|The group ID which the bot will be sending *"draft"* commit messages that, if accepted, will be sent to the configured channel. To obtain that you can use the `/chatid` command in the group chat, while the bot is inside and administrator.
channelID|String|The channel which the bot will be sending commit messages that were previously accepted. The bot **MUST** be an administrator.
admin|Array\<Number\>|An array containing userIDs of those who will be able to execute admin commands on the bot.
language|String|The language code that directly correseponds with the file name in the languages folder. `Example: lang/it.json -> language: "it"`

## FAQ 

*wip*
