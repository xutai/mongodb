



### dump

make sure setting environment variables like this C:\Program Files\MongoDB\Server\4.2\bin

using command prompt

using [reference             > mongodb             package components > mongodump ](https://docs.mongodb.com/manual/reference/program/mongodump/#bin.mongodump)



directly type `mongodump` in cmd input line

something like this `C:\Users\Administrator>mongodump`

then logs

```
2020-05-14T22:41:28.199+0800    writing admin.system.version to
2020-05-14T22:41:28.203+0800    done dumping admin.system.version (1 document)
2020-05-14T22:41:28.203+0800    writing xutai.xutaiaaaaa to
2020-05-14T22:41:28.204+0800    done dumping xutai.xutaiaaaaa (0 documents)
2020-05-14T22:41:28.506+0800    writing xutai.dfgsdfgdfg to
2020-05-14T22:41:28.508+0800    done dumping xutai.dfgsdfgdfg (0 documents)
```

check the folder **C:\Users\Administrator\dump**, you will see files 



### restore

using [reference             >             mongodb package components > mongorestore](https://docs.mongodb.com/manual/reference/program/mongorestore/)

move the dbs folder into the dump directory

try drop the database, either by using shell or mongo compass

```
C:\Users\Administrator>mongorestore dump/
2020-05-14T23:17:32.392+0800    preparing collections to restore from
2020-05-14T23:17:32.398+0800    reading metadata for xutai.xutaiaaaaa from dump\xutai\xutaiaaaaa.metadata.json
2020-05-14T23:17:32.407+0800    restoring xutai.xutaiaaaaa from dump\xutai\xutaiaaaaa.bson
2020-05-14T23:17:32.412+0800    no indexes to restore
2020-05-14T23:17:32.412+0800    finished restoring xutai.xutaiaaaaa (1 document, 0 failures)
2020-05-14T23:17:32.413+0800    1 document(s) restored successfully. 0 document(s) failed to restore.
```

but if try this

```
C:\Users\Administrator>mongorestore dump/xutai/
2020-05-14T23:28:12.221+0800    preparing collections to restore from
2020-05-14T23:28:12.223+0800    don't know what to do with file "dump\xutai\xutaiaaaaa.bson", skipping...
2020-05-14T23:28:12.224+0800    don't know what to do with file "dump\xutai\xutaiaaaaa.metadata.json", skipping...
2020-05-14T23:28:12.224+0800    0 document(s) restored successfully. 0 document(s) failed to restore.
```

yeah, so maybe i should delele some records if i don't want to restore from        this        forder?

