From https://github.com/epfl-dojo/telegram-coreos-update

1. docker run command in dockerfile

2. Modify the dockerfile

a. line12: FROM node

b. add line "COPY secrets.json /usr/src/app/"

c. add the followiing code
```
app.command('hello', (ctx) => {
    return ctx.reply('Receive word hello')
})
```
3. docker build -t abc .

Telegram CoreOs update bot
A telegram bot which send CoreOs updates [@CoreOSbot](https://t.me/CoreOSbot)

When running [...] you will be able to use some of these commands:
  * `/latest` → will pop a inline keyboard with options
    * `alpha`
    * `beta`
    * `stable`
  * `/latest alpha` | `/alpha`
  * `/latest beta` | `/beta`
  * `/latest stable` | `/stable`

# Idea
Use the channel https://t.me/coreosupdate to broadcast new release.

## Secrets
Create a file `secrets.json` with the Telegram token:
```
{           
  "token": "123456789:ABCDEFGHIJKLMNOPKRSTUVWXYZ123456789"
}
```
