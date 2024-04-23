a. How many data your publlsher program will send to the message broker in one run?

- In the main.rs file, we are publishing five events of type UserCreatedEventMessage to the message broker. So, the publisher program will send five data messages to the message broker in one run. Each call to publish_event sends one event.

b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

- If the URL "amqp://guest:guest@localhost:5672" is used in the publisher program, it means that the publisher program is also configured to connect to the same AMQP server running on the local machine.

## Running RabbitMQ as message broker.

![alt text](image.png)

## Monitoring chart based on publisher

![alt text](image-1.png)

I ran publisher 3 times, which is why there are 3 spikes in this photo. The reason there are 3 spikes is that it corresponds to the 3 times I ran the publisher. 

## Simulation Slow Subscriber

![alt text](image-4.png)

My queued messages is 10. I got this after running cargo run 3 times. I believe this is because while the initial 5 messages were run, the other two instasnces of cargo run makes it so that the other 10 messages need to be queued first. 