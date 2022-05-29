# ASGI (Asynchronous Server Gateway Interface)

- ASGI is a structured, asynchronous callable
- It takes
  - a `scope`, a `dict` containing details about the specific connection
  - `send` an asynchronous callable to send event messages to the client
  - `receive` an asynchronous callabe to receive event messages from the client
- Every event sent or receive is a `dict`
  - an event has `type` key to refer event structure
