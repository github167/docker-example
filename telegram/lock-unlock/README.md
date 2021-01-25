From https://hub.docker.com/r/edjopato/telegramlockbot (https://github.com/EdJoPaTo/telegramLockBot)

1. echo your_token > bot-token.txt

2. docker pull edjopato/telegramlockbot

3. docker create --name temp_container edjopato/telegramlockbot

4. docker cp bot-token.txt temp_container:/app/bot-token.txt

5. docker commit temp_container edjopato/telegramlockbot

6. docker system prune

7. docker run --rm edjopato/telegramlockbot cat /app/bot-token.txt

Run:

1. docker run --rm -d --name one edjopato/telegramlockbot

Another method:

1. git clone https://github.com/EdJoPaTo/telegramLockBot; cd telegramLockBot

2. echo your_token > bot-token.txt

3. add "COPY bot-token.txt /app" in Dockerfile

4. rename the bot-token.txt in .dockerignore to xbot-token.txt

5. docker build -t lockbot .

6. docker run --rm -d --name one lockbot
