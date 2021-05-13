# Socket.IO V4.x Notlar

## Volatile events
- Volatile events are events that will not be sent if the underlying connection is not ready (a bit like [UDP](https://fr.wikipedia.org/wiki/User_Datagram_Protocol), in terms of reliability).
- This can be interesting for example if you need to send the position of the characters in an online game (as only the latest values are useful).
- **Another use case is to discard events when the client is not connected (by default, the events are buffered until reconnection).**

## Acknowledgements
- Events are great, but in some cases **you may want a more classic request-response API**. In Socket.IO, this feature is named acknowledgements.

## Manager
- The `Manager`  _manages_ the Engine.IO [client](https://github.com/socketio/engine.io-client/) instance, which is the low-level engine that establishes the connection to the server (by using transports like WebSocket or HTTP long-polling).

https://socket.io/docs/v4/middlewares/
https://socket.io/get-started/private-messaging-part-4/
https://socket.io/docs/v4/client-api/#socket-id (emit to specific visitor with socketid)
