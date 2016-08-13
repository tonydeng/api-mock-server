# API-Mock-Server Docker image

Run a  api-blueprint Document application in docker.

> Document your API in the API blueprint format, and API-Mock mocks your routes and sends the responses defined in the api spec.

See more about the application: https://github.com/localmed/api-mock

## Docker Run Example


### Run Default Example

```bash
docker run -it -p 3000:3000 wolfdeng/api-mock-server
```

### Select API Document

```bash
docker run -it -v $PWD/api.md:/etc/secrets/api.md -p 3000:3000 wolfdeng/api-mock-server
```


## API-Blueprint Example

[API Blueprint Example](example/api.md)

```api-blueprint
FORMAT: 1A
HOST: https://wolfdeng.info

# Group API Blueprint Example

# Hello World [/]

API Blueprint Example entry point.

## Retrieve Entry Point [GET]

+ Response 200 (text/plain)

    Hello World!

# Group Messages


# Data Structures

## Message(object)

+ id:1 (required,number) - Unique identifier
+ title: Good Event (required) - Single line description
+ body: This is good event body - Full descroption of the message body.


## MessageList(array)
+ (Message)

## Messages [/message]

### List Messages [GET]

+ Response 200 (application/json)

    + Attributes (MessageList)

## A Single Message [/message/{id}]
Message description

+ Parameters

    + id: `1` (required, number) - The message ID

### Get Message [GET]

+ Response 200 (application/json)

    + Attributes (Message)
```
