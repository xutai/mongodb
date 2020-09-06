
> "index" is the name of db "pcgames"

```shell
db.index.bulkWrite(
    [
        {
            updateMany: {
                "filter": {},
                "update": {
                    '$set': {
                        'price': 0
                    }
                }
            }
        }
    ]
)
```
```shell
db.index.bulkWrite(
    [
        {
            updateMany: {
                "filter": {
                    'price': {
                        '$ne': 0
                    }
                },
                "update": {
                    '$set': {
                        'price': 11
                    }
                }
            }
        }
    ]
)
```


