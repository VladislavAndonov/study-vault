# Pub-Sub Pattern

Pub-sub is a message pattern design to communicate messages between system components without any of them knowing about each other's existence.

## 1. Core Components
### Senders (Publishers):
- Creates a message when an event occurs.
- Has no knowledge about the subscribers.
- Sends the message to the broker instead directly to the consumers.

### Receivers (Subscribers):
- Register interest in specific events or topics.
- Receive and process messages when they are published.
- One event can have multiple subscribers.

### Message Broker (Event Bus):
- Receive published messages.
- Forwards them to the subscribers who are registered to receive them

## 2. Advantages
### Loose Decouplyng:
- Publishers and subscribers can communicate without direct dependencies.

### Scalability:
- Easy to add more publishers or subscribers without impacting the system.

### Flexibility:
- Subscribers can dynamically choose which messages to listen to.

### Asynchronous:
- Subscribers can process messages at their own pace, improving system responsiveness.

