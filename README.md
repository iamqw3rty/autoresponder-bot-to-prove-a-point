# This is an auto-responder bot I made to prove a point to `sound#0001`. Please follow the instructions or I will come to your house and break your shins.


# Dependencies

- Node.js
- NPM

## Creating the bot

I'm assuming you know how to create a bot already on the Discord developer portal. If you don't, here's an image guide on how to:
![Image instructions](https://i.imgur.com/mWD7nS5.png)

## Configuration

To configure the bot, open `/botconfig/config.json` and input your bot token in the space provided. You may also optionally change the prefix. Next, open `/botconfig/settings.json` and input the owner ID and whitelisted channels in the spaces provided.

## Installing bot dependencies

To install the bot's dependencies, first run `npm i`, then run `npm install ejs multer express`.

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
