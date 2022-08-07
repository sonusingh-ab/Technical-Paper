# Message queues and its benefit

The principal of message queue is that client application called producer create message and place it in queue which is stored in there until another application called consumer retrieves it. In simple word both applications work independently.

A message queue provides an asynchronous communications protocol,which is a system that puts a message onto a message queue and does not require an immediate response continuing processing. Email is the best example to understand asynchronous communication. When an email is sent the sender continues to process other things without needing an immediate response from the receiver. This way of handling message is known as decoupling.

Let's understand it with the help of an example, imagine a web service that gets a lot of message requests every second and it needs to process all the request as it receive and can't loose any request so in this case it is ideal to use queue between web service and processing service. When web service receive a request it can put "start processing" message on queue and other process can take place and handle messages in order.

1. Message queues enable asynchronous communication means the producer and the consumer are not interacting with each other.

2. Queues make your data persistent and reduce the errors when your different part of system go offline. Queues make your system more error tolerant because if one system goes offline, the other system will still interact with queue.

3. Message queues remove dependencies between components and simply the code for the decoupled applications and focus is given on to develop discrete business logics.

## Message queue popular tools

* Kafka

* RabbitMQ

* Amazon SQS

* Celery

* MQTT

* ActiveMQ

## Enterprise message bus

Enterprise message bus also known as enterprise service bus is a software platform used to distribute work among connected components of an application. Think of ESB as a set of switches which directs messages along a specific route between applications and/or components according to business policy. Because an ESB controls the way work moves, it makes easy to add components to an application or change components. ESB also provides load balancing by instantiating multiple copies of component to improve performance as well as failover support when a component or resource fail. ESB implements a communication system between mutually interacting software applications in a service oriented architecture.

The ESB is implemented in software that operates between business applications, and enables communication between them. Ideally ESB should replace communication between all the component applications. To achieve this objective, ESB must encapsulate all the functionality of the component applications. The message model defines a standard set of messages that the ESB can receive and transmit. The message that ESB receive, transmits it to the appropriate application. Often because that application are evolved without the same message model, the ESB has to transform it into a format that the application can intercept with the help of software adapter.

### Functions of enterprise message bus

1. Route messages between services

2. Resolve contention between communicating service components

3. Control deployment and versioning of services

4. Marshal use of redundant services

#### References section

* <https://en.wikipedia.org/wiki/Enterprise_service_bus>

* <https://www.techtarget.com/searchapparchitecture/definition/Enterprise-Service-Bus-ESB#:~:text=An%20enterprise%20service%20bus%20(ESB,structural%20and%20business%20policy%20rules>

* <https://stackshare.io/message-queue>

* <https://aws.amazon.com/message-queue/benefits/#:~:text=Message%20queues%20provide%20communication%20and,in%20a%20fanout%20design%20pattern>.

* <https://www.cloudamqp.com/blog/what-is-message-queuing.html>
