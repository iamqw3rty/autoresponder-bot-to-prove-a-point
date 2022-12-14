### What happens when a transfem with zero programming experience and WAY too much time on their hands gets hold of an archived repository? You get this ungodly creation. Welcome to hell, kids.
# Dependencies

- Git
- Node.js
- npm

## Creating the bot

I'm assuming you know how to create a bot already on the Discord Developer Portal. If you don't, here's an image guide on how to:
![Image instructions](https://i.imgur.com/mWD7nS5.png)

## Configuration

Before you do anything, you need to clone the repository. To do that, you must run `git clone https://github.com/iamqw3rty/autoresponder-bot-to-prove-a-point.git && cd autoresponder-bot-to-prove-a-point` (the command may vary from OS to OS, these are the instructions for Ubuntu 22.04). To configure the bot, open `/botconfig/config.json` and input your bot token in the space provided. You may also optionally change the prefix. Next, open `/botconfig/settings.json` and input the owner ID and whitelisted channels in the spaces provided.

## Installing bot dependencies

To install the bot's dependencies, just run `npm i`. There is a chance that the bot will error out due to unmet dependencies. If that happens, simply run `npm install ejs multer express`.

## Setting up the dashboard

To setup the dashboard, set the `dashboardPort` in `/botconfig/settings.json` to the port you want the dashboard to run on. Then, you can view the dashboard at `http://localhost:{port}` once the bot is running.

## Running the bot

To run the bot, make sure you are in the bot's directory, then run `node index.js`. If all goes well, the bot should be running!

## Adding more auto responses - MANUAL

To add more auto responses, you will need to add a new file to the `autoresponse` folder. The file name should be a single word describing the response. The file should contain a list of phrases to respond to. Here is an example:

```json
{
  "name": "offlineModeWarning",
  "type": "string",
  "triggers": ["SERVER IS RUNNING IN OFFLINE/INSECURE MODE!"],
  "responses": [
    "Hey! This is just a warning to tell you that your server is running in the offline mode to allow cracked players to join. There is nothing to worry about!"
  ]
}
```
