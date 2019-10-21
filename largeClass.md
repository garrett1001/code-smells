# Large Class

```{programming language}
class Card:
      def __init__(self, name, url, picUrl, address, phone):
        self.name = name
        self.url = url
        self.picUrl = picUrl
        self.address = address
        self.phone = phone
```

This class needs to get rid of address and phone and just access those from an agencies models from the database.