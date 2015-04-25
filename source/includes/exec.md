# Docker exec

__Available only on the Stream API__

This endpoint its executes docker exec in a container.

This endpoint opens a duplex websocket in which you can send input to a command been executed inside a container and a get the output of that command.

```http
GET /v1/container/:uuid/exec?command=bash&user=username&token=apikey HTTP/1.1
Host: stream.tutum.co
Connection: Upgrade
Upgrade: websocket
```

### Websocket Request

`GET /v1/container/:uuid/exec`

Listens for new Tutum Events

### Query Parameters

Parameter | Description
--------- | ----------- 
command | This is the command that will be executed inside a container. Default is `bash`.

