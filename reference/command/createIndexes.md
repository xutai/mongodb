
```

db.users.createIndex(
    { location: "2d"}
)

db.users.createIndex(
    { location: "2dsphere"}
)


db.users.createIndex(
   {collation: {locale: "simple"}}
)
 
```