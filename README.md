# REST API CRUD

 > Endpoint address: `$host_addr:$port/profiles/:id`

This example demonstrates how to use Go kit to implement a REST-y HTTP service.
It leverages the excellent [gorilla mux package](httpsgithub.comgorillamux) for routing.

Run the example with the optional port address for the service 

```bash
$ go run .cmdprofilesvcmain.go -http.addr 8080
ts=2018-05-01T161312.849086255Z caller=main.go47 transport=HTTP addr=8080
```

Create a Profile

```bash
$ curl -d '{id1234,NameGo Kit}' -H Content-Type applicationjson -X POST httplocalhost8080profiles
{}
```

Get the profile you just created

```bash
$ curl localhost8080profiles1234
{profile{id1234,nameGo Kit}}
```