[https://docs.mongodb.com/manual/reference/program/mongod/](https://docs.mongodb.com/manual/reference/program/mongod/)



logs
```
vi /var/log/mongodb/mongod.log
```

dbpath
```
dbpath=/var/lib/mongo 

config
```
/etc/mongod.conf
```
 ```

```
vi /lib/systemd/system/mongod.service
/usr/bin/mongod --config /etc/mongod.conf
```




shutdown the mongod process
```
mongod --shutdown
```


```
 mongod --dbpath /var/lib/mongo --logpath /var/log/mongodb/mongod.log --fork
 ```