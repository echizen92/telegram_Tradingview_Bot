# telegram_Tradingview_Bot


Create Telegram Bot

Find BotFather and issue command /newbot
Provide bot name
Provide bot username - unique and ends with _bot

Once bot is created, you will get a message with token access key in it. Store the token access key.

Prepare Telegram Channel

Create new telegram channel
Add the bot @username_to_id_bot to it as admin and issue /start to find chat id
Store the chat id and dismiss @username_to_id_bot from channel
Find the bot created in previous step using bot username and add it to channel as admin

Setup replit
Set environment variables - TOKEN and CHANNEL which are acquired from previous steps.
Run the REPL


From telegrambot.py
```
tg_bot = Bot(token=os.environ['TOKEN'])
channel = os.environ['CHANNEL']
```

Test with postman

Use the URL on repl and create web-hook post request URL by adding /webhook to it.
Create post request on postman and send it.
You can see that messages sent via postman appearing in your telegram channel.
append ?jsonRequest=true if you are using json output from alerts.

Test out POST command using baseurl

```
http://xxxxx.xxxx.repl.co/webhook?jsonRequest=true&tblfmt=fancy_grid&chart=0XoCxnwn&loginRequired=false
```

To display screenshot of invite only scripts login is required. 

Set alerts from tradingview to web-hook

Use web-hook option and enter the webhook tested from postman in the web-hook URL

