# node-docker

## Installation
```
npm i
```

## Run server
```
node server.js
```

## Request examples
```
curl --request POST \
  --url http://localhost:8000/test \
  --header 'content-type: application/json' \
  --data '{
	"msg": "testing"
}'
{
    "code": "success",
    "payload": [
        {
            "msg": "testing",
            "id": "31f23305-f5d0-4b4f-a16f-6f4c8ec93cf1",
            "createDate": "2020-08-28T21:53:07.157Z"
                }
            ]
        }
```

```
curl http://localhost:8000/test
    {
        "code": "success",
        "meta": {
            "total": 1, 
            "count": 1
        },
        "payload": [
            {
                "msg": "testing",
                "id": "31f23305-f5d0-4b4f-a16f-6f4c8ec93cf1",
                "createDate": "2020-08-28T21:53:07.157Z"
        }
]}
```

## Build image
```
docker build --tag node-docker .
```

## Run container
```
docker run -d -p 8000:8000 node-docker
```
