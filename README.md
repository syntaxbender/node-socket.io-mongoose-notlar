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

https://stackoverflow.com/questions/4647348/send-message-to-specific-client-with-socket-io-and-node-js

alakasız ama güzel başlık => https://stackoverflow.com/questions/29794964/how-do-webrtc-peers-connect-to-each-other-if-none-have-opened-ports

# Mongoose Notlar
https://www.bezkoder.com/mongodb-many-to-many-mongoose/

https://javascript.plainenglish.io/store-clean-data-by-validating-models-with-mongoose-f6453dbdbff9

https://mongoosejs.com/docs/validation.html

https://mongoosejs.com/docs/middleware.html#error-handling-middleware
```
Athlete.
  find().
  where('sport').equals('Tennis').
  where('age').gt(17).lt(50).  //Additional where query
  limit(5).
  sort({ age: -1 }).
  select('name age').
  exec(callback); // where callback is the name of our callback function.
```
https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/mongoose#mongoose_primer

https://stackoverflow.com/questions/51391080/handling-errors-in-express-async-middleware >> Express Async Error Handling Middleware Explanation/Discussion

https://zellwk.com/blog/async-await-express/ >> Mongoose Error Handling in Express (Not Express Middleware)

https://levelup.gitconnected.com/handling-errors-in-mongoose-express-for-display-in-react-d966287f573b >> Express Middleware is not supporting async method for handling errors.

https://mongoosejs.com/docs/connections.html >> Not work for "ValidationError"
```
//Not work for "ValidationError"
mongoose.connection.on('error', err => {
  logError(err);
});
```

# Express notlar

https://expressjs.com/en/guide/error-handling.html
