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