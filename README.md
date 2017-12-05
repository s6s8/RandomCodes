# RandomCodes

### Python
#### Read Online File
```
#! /usr/bin/env python

try:
    # For Python 3.0 and later
    from urllib.request import urlopen
except ImportError:
    # Fall back to Python 2's urllib2
    from urllib2 import urlopen

html = urlopen("http://www.google.com/") # .read().decode('utf-8')
# html = html.read().decode('utf-8')
print(html.read())
```

