# jakeybot-container-compose
Docker-compose files for [Jakeybot](https://github.com/zavocc/JakeyBot) chatbot with discord integration.

(podman-compose to follow after testing)

## Preparation

### Setup your own discord bot

You can follow [this guide](https://discordjs.guide/preparations/setting-up-a-bot-application.html#creating-your-bot) for creating a discord bot on the [Discord 
Developer Portal](https://discord.com/developers/applications).

You will need to get a token, configure pictures etc.

## Configure Containers

### 1. Clone the repo locally

```
git clone https://github.com/bretton/jakeybot-container-compose
cd jakeybot-container-compose
```

### 2. Configure the environment variables by copying the sample

```
cp default.env .env
```

and edit `.env` for the following variables:
* TOKEN
* GEMINI_API_KEY / OPENAI_API_KEY etc
* BOT_NAME

and make sure to update the password in this line if changed in the `docker-compose.yml` file.
* MONGO_DB_URL

### 3. Run Jakeybot

Run with
```
docker-compose up -d
```

### 4. Stop Jakeybot

Stop with 
```
docker-compose down
```
