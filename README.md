## Network
```
                          _______
          +-----+        |       |
          |User |------->| SS7   |
          |Device|       |Network|
          +-----+        |       |
                         |       |
                         |       |
          +-----+        |       |
          |User |<-------| SS7   |
          |Device|       |Network|
          +-----+        |       |
                         |       |
                         |       |
                         |_______|
```
In this illustration, there are two user devices connected to an SS7 network. The user devices can be any devices capable of sending or receiving SS7 messages, such as mobile phones or telecommunication switches.
The user devices communicate with each other by exchanging SS7 messages through the SS7 network. The SS7 network is responsible for routing and delivering these messages between the sender and recipient devices.

## Packet
```
+-----------------+
|       Header    |
+-----------------+
|      Routing    |
|    Information  |
+-----------------+
|    Parameters   |
|    (optional)   |
+-----------------+
```

## SMS Example using SS7
```
+-----------------+
|    Header       |
+-----------------+
| Routing Info    |
| DPC: 1234       |
| OPC: 5678       |
+-----------------+
|    MAP Header   |
| Operation: SMS  |
+-----------------+
|    MAP Body     |
| Sender: +123456 |
| Recipient: +789 |
| Message: Hello! |
+-----------------+
```
- Header: The header contains control information about the SS7 message.
- Routing Information: The routing information specifies the Destination Point Code (DPC) as 1234 and the Originating Point Code (OPC) as 5678.
- MAP Header: The MAP header indicates that the operation being performed is related to SMS.
- MAP Body: The MAP body carries the SMS-related parameters:
- Sender: The sender's phone number is represented as +123456.
- Recipient: The recipient's phone number is represented as +789.
- Message: The content of the SMS is "Hello!"
