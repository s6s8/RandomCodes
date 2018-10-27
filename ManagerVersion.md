`docker exec mversion nohup python3 app.py &`

```
import time
try:
    # For Python 3.0 and later
    from urllib.request import urlopen
except ImportError:
    # Fall back to Python 2's urllib2
    from urllib2 import urlopen

# Send message that bot Started
htmlx = urlopen("https://api.telegram.org/botAPI/'
    'sendmessage?text=Started.&chat_id=CHATID")

#sebds a white true command to the bot to open the manager.io URL, read it and decode it.
while True:
    html = urlopen('https://www.manager.io/version.txt') # .read().decode('utf-8')
    html = html.read().decode('utf-8')

    file = open('version.txt', 'r')
    manver = file.read().rstrip()
    file.close()
    # print(manver)

#sends command to telegram bot, opens the version, write the html and closes, then opens the botAPI, prints and sleeps.
    if html != manver:
        fo = open('version.txt', 'w')
        fo.write (html)
        fo.close()
        print("Version Changed: ")
        html2 = urlopen("https://api.telegram.org/botAPI/' \
            'sendmessage?text=New%20Version:%20" + html + "&chat_id=CHATID")
    time.sleep(86400)
    # print(html)
    # time.sleep(10)

```

```
PULL REQUEST TRIAL
```
