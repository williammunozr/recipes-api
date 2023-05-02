# Recipes API with Gin

## Installing Dependencies

### xis to generate a unique ID

```commandline
$ go get github.com/rs/xid
```

### Installing Go Swagger

```commandline
brew tap go-swagger/go-swagger
brew install go-swagger
```

#### Validate the Swagger version

```commandline
swagger version                                                                                              ─╯
version: v0.30.3
commit: ecf6f05b6ecc1b1725c8569534f133fa27e9de6b
```

#### Generate a spec file

```commandline
swagger generate spec -o ./swagger.json
```

## Installing MongoDB Community Edition

### Installing Atlas Version

```commandline
$ brew install mongodb-atlas
$ atlas setup
```

### Installing MongoDB Community Locally

```commandline
$ sudo dpkg -i mongodb-org-server_6.0.5_amd64.deb
```

### Start MongoDB

```commandline
$ sudo systemctl start mongod
```

### Start MongoDB at system reboot

```commandline
$ sudo systemctl enable mongod
```

### Verify that MongoDB has started successfully

```commandline
$ sudo systemctl status mongod
```

### Installing MongoDB Compass

```commandline
$ sudo dpkg -i mongodb-compass_1.36.4_amd64.deb
```

### Installing Mingo MongoDB GUI

```commandline
$ sudo dpkg -i mingo_1.12.1_amd64.deb
```

## Installing MongoDB Go Driver

```commandline
$ go get go.mongodb.org/mongo-driver/mongo
```

## Configuring MongoDB URI and Database

I'm not using a password for now.

```commandline
export MONGO_URI="mongodb://localhost:27017/test?authSource=admin"
export MONGO_DATABASE="gin-recipes"
```

## Redis Installation

```commandline
$ sudo apt install lsb-release
$ curl -fsSL https://packages.redis.io/gpg | sudo gpg --dearmor -o /usr/share/keyrings/redis-archive-keyring.gpg
$ echo "deb [signed-by=/usr/share/keyrings/redis-archive-keyring.gpg] https://packages.redis.io/deb $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/redis.list
$ sudo systemctl status redis-server
```


## References

- [Globally Unique ID Generator](https://github.com/rs/xid)
- [Swagger Meta Configuration](https://goswagger.io/use/spec/meta.html)
- [MongoDB Community Edition](https://www.mongodb.com/try/download/community)
- [MongoDB Go Driver](https://github.com/mongodb/mongo-go-driver)
- [Mingo MongoDB GUI](https://github.com/mingo-app/mingo/releases)
