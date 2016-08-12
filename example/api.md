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
