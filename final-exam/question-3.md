# Question 3
## Problem
Suppose an instance of MongoClient is created with the following settings:

import { MongoClient } from "mongodb"

const URI = "mongodb+srv://m220-user:m220-pass@m220-test.mongodb.net/test"

const testClient = await MongoClient.connect(
  URI,
  { connectTimeoutMS: 100, retryWrites: true, useNewUrlParser: true },
)

const clientOptions = testClient.s.options

Which of the following tests will pass?

Check all answers that apply:

expect(clientOptions.retryWrites).toBe(true)

expect(clientOptions.ssl).toBe(false)

expect(clientOptions.authSource).toBe("admin")

expect(clientOptions.user).toBe("mongo-admin-user")

expect(clientOptions.connectTimeoutMS).toBe(50)

### My answer
expect(clientOptions.retryWrites).toBe(true)
expect(clientOptions.ssl).toBe(false)

### The correct answer
So close. This was the only question I missed.

expect(clientOptions.authSource).toBe("admin")
expect(clientOptions.retryWrites).toBe(true)

+ By default, MongoClient objects will authenticate against the admin database. To use the login credentials stored on another database., we can add authSource=<some-other-DB> at the end of the URI string.
+ Because we passed retryWrites: true to our MongoClient.connect() statement, this variable is set to true for any query issued using this connection.

For the other options...
+ Because we used an SRV string, SSL is enabled by default for this connection.
+ Because we connected as m220-user (denoted in the URI string), the value of this variable would not be mongo-admin-user.
+ Because we specified connectTimeoutMS: 100 in MongoClient.connect(), the value of this variable would be 100, not 50.