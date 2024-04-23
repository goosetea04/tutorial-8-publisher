a. How many data your publlsher program will send to the message broker in one run?

- In the main.rs file, we are publishing five events of type UserCreatedEventMessage to the message broker. So, the publisher program will send five data messages to the message broker in one run. Each call to publish_event sends one event.

b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

- If the URL "amqp://guest:guest@localhost:5672" is used in the publisher program, it means that the publisher program is also configured to connect to the same AMQP server running on the local machine.