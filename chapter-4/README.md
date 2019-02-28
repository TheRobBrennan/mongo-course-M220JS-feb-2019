# Welcome
Chapter 4 of this course is focused on resiliency. Specifically on Connection pooling, error and timeout handling, and principle of least privilege.

## Ticket: Connection Pooling
Modify `mflix-js/src/index.js` and `mflix-js/test/config/mongoEnvironment.js` so that the maxium size of the connection pool is fifty (50) connections and that `mflix-js/test/connection-pooling.test.js` passes. Verify by running:
```
$ npm test -t connection-pooling
```

## Ticket: Timeouts
Modify `mflix-js/src/index.js` and `mflix-js/test/config/mongoEnvironment.js` to set a write timeout of 2500 milliseconds and so that `mflix-js/test/timeouts.test.js` passes. Verify by running:
```
$ npm test -t timeouts
```
