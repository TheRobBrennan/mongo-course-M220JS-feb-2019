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

## Ticket: Handling Errors
Modify `mflix-js/src/dao/moviesDAO.js` so that `getMovieByID()` returns null when an `InvalidId` error is thrown  and `mflix-js/test/error-handling.test.js` passes. Verify by running:
```
$ npm test -t error-handling
```

## Ticket: Principle of Least Privilege
For this ticket, you'll be required to add a new user on your Atlas cluster for the MFlix application to connect with.

The user should follow credentials:

  username: mflixAppUser
  password: mflixAppPwd

This user should have the `readWrite` role on the mflix database. Use `Add Default Privileges` to assign the user this specific role.

After you have created this user, modify the SRV connection string in your configuration file so the application connects with the new username and password.

There are no unit tests for this ticket.
