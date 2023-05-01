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

## References

- [Globally Unique ID Generator](https://github.com/rs/xid)
- [Swagger Meta Configuration](https://goswagger.io/use/spec/meta.html)
