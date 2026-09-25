# SlackMate 🤖

SlackMate is a custom Slack bot built with **JavaScript**, **Node.js**, and **Slack Bolt**.

It uses **Slack Socket Mode** to receive slash commands without requiring a public web server. SlackMate is hosted on **Hack Club Nest** and runs continuously using **PM2**.

## Features

* ⚡ Check bot response latency
* 📖 Display available commands
* 🐱 Fetch random cat facts from an external API
* 🔌 Uses Slack Socket Mode
* ☁️ Hosted on Hack Club Nest
* ♻️ Managed with PM2 for continuous operation

## Commands

| Command              | Description             |
| -------------------- | ----------------------- |
| `/slackmate-ping`    | Check bot latency       |
| `/slackmate-help`    | Show available commands |
| `/slackmate-catfact` | Get a random cat fact   |

## Tech Stack

* JavaScript
* Node.js
* Slack Bolt
* Slack Socket Mode
* Axios
* dotenv
* PM2
* Hack Club Nest

## How It Works

1. A user runs a SlackMate slash command.
2. Slack sends the command to the bot through Socket Mode.
3. SlackMate processes the request.
4. For API-based commands, the bot requests data from the external API.
5. SlackMate sends the result back to Slack.

## Running Locally

Install the dependencies:

```bash
npm install
```

Create a `.env` file:

```env
SLACK_BOT_TOKEN=xoxb-your-bot-token
SLACK_APP_TOKEN=xapp-your-app-token
```

Then start the bot:

```bash
node index.js
```

## Deployment

SlackMate is deployed on **Hack Club Nest**.

PM2 keeps the Node.js process running:

```bash
pm2 start index.js --name SlackMate
pm2 save
```

PM2 is configured to start automatically when the server boots, allowing SlackMate to remain online even when the developer's computer is turned off.

## Security

Slack tokens are stored in `.env` and are **not committed to GitHub**.

The `.env` file is included in `.gitignore`.

## Project

Built as a Hack Club Stardance mission project.

GitHub: https://github.com/Ayan3107/SlackMate
