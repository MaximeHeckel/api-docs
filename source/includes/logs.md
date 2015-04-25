# Logs

> Example

```json
{
	"type": "log",
	"log": "logLine"
}
```

__Available only on the Stream API__

Logs endpint opens a websocket to follow the logs of a container.

```http
GET /v1/container/:uuid/logs?tail=100&user=username&token=apikey HTTP/1.1
Host: stream.tutum.co
Connection: Upgrade
Upgrade: websocket
```


### Websocket Request

`GET /v1/container/:uuid/logs`

Listens for logs from a container

### Query Parameters

Parameter | Description
--------- | ----------- 
tail | Amount of lines that are tailed once the connection is open. Default is 300.

