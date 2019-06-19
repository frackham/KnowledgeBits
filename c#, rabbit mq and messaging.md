## rabbit
See test project.

easynetq is .net implementation of rabbit.

rabbitmqtools powershell module.

### amqp
look up syntax



## azure messaging service bus

### storage queues

cheap.
getput,peek.
80gbmsx.



### service bus
amqp
at most once
service bus explorer (tool). wysiwyg for service bus

query params are properties, not part of message. multiple query types including sqlm
dead letter queue on error.


### event grid / event hubs
for scale



### functions
scale out of the box.
execute limited to 5 min.
try online (functions.azure.com/try).
send function/ calc function.



## architecture
John staveley
get slides for messaging diagrams.
slides are here: https://www.slideshare.net/johnstaveley/messaging-rabbitmq-azure-service-bus-docker-and-azure-functions , code here: https://github.com/johnstaveley/MessagingPresentation , any questions to Twitter: @johnstaveley

### one way
still scale improvement over .
competing consumers
consumer polling

### rpc
occasionally connecting systems.


### response request



### pub sub
facets/topics

### routing


### scatter gather


## reliability patterns
1. Sent, q dies. message is.lost.
1. Consumer doesn't pick ipessages.

acknowledgement levels
persist queues to disk
connection fail (heartbeats).
set ack on produce

use a (true) service bus (reliability, retry).
saga = transaction across messages.

## event sourcing
append only (state = sum of events)
replay




## docker
kitematic UI.

