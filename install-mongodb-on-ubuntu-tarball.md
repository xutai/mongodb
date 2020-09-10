[Install MongoDB Community on Ubuntu using .tgz Tarball](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu-tarball/)



### Localhost Binding by Default

- configuration file with bindIp

```
cd /etc/
vi mongod.conf
...change the bindIp to  172.18.122.187
esc :q or :qw
mongod --config /etc/mongod.conf

```



> doesn't work event i've configured it?!

- command-line argument --bind_ip

[reference - mongodb package components - mongod](https://docs.mongodb.com/manual/reference/program/mongod/#cmdoption-mongod-bind-ip)

```
mongod --bind_ip 127.0.0.1 --port 27017
mongod --bind_ip 172.18.122.187 --port 27017
pm2 start mongod --name mongod
pm2 start mongod --name mongod
pm2 start mongod --bind_ip 172.18.122.187 --port 27017 --name mongod  -- not working
```


