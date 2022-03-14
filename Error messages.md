# Error Messages

Key info to include in error messages are
  - Context, the situation in which error occurs
  - Error itself, what happened
  - Mitigation, what can be done to correct itself

This is for error messages of libraries and frameworks. For user facing error
messages, it is best not to expose internal workings.

## Context

Error message is akin to telling a story so establish context before giving what
the error is. The message shoud tell what the code is trying to do when the
error occurs.

For error messages related to file processign or configuration files, it is
better to include absolute path of file in the message. But for mulit-tenant for
SaaS scenarios, it's best to regard those as confidential information.

If the framework support different file types, the file type in question should
be in error message as well.

Many logging frameworks suppor the idea of [[Mapped Diagnostic Context(MDC)]]
which is map data structure to send key/value pairs to the log message. If the
error message is to show up in logs, set context information to MDC.

[[Structured Logging]] in the form of JSON to put context information into
separate attributes of log entry can make consumers of logs filter and use only
what is required for them.

For exception error messages, chain of exceptions until the last one is
important context so the whole chain shoud be stored.

## Error Itself

Try to be consise and efficient describing what the error is. Prepare long one
and short one, the usage of which can be controlled by ```verbose``` level.

## Mitigation

What can be done to overcome the error? For longer information, point to a URL
of stable reference inforamtion. Another idea is to provide error codes for easy
search on web and forums.

## General Best Practices

- Have uniform voice and style
- One concept, one term. Don't use different terms for one concept. Don't use
  same term for different topics.
- Don't localize error messages (don't translate to other languages than
  English)
- Don't make error messages an API contract. Consumers of API should not be
  forced to parse error messages. Instead raise an exception with
  machine-processable code.
- Take note of exposing sensitive data. Don't create scenarios where privacy
  should be a concern.
- Either raise an excepiton or log an error but NOT BOTH to avoide logging the
  same error twice.
- Fail early. Quicker feedbacks can shorten time for fixes
  
## Reference

- [What's in a Good Error Message](https://www.morling.dev/blog/whats-in-a-good-error-message/)

