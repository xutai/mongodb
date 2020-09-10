

```
2020-09-09T12:27:37.248+0800 I STORAGE  [initandlisten] exception in initAndListen: DBPathInUse: Unable to lock the lock file: /var/lib/mongo/mongod.lock (Resource temporarily unavailable). Another mongod instance is already running on the /var/lib/mongo directory, terminating
```

try
```
rm mongod.lock
```


```
connection: Version incompatibility detected: unsupported WiredTiger file version: this build requires a maximum version of 2, and the file is version 3: WT_ERROR: non-specific WiredTiger error
```