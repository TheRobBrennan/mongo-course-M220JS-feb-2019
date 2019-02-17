# Welcome
Chapter 1 focuses on getting the mflix application up and running on your local development machine. Once the initial setup is complete, I would love to Dockerize this project so that it can run in its own containerized process for development.

## Initial setup
Make sure that you have the following setup and configured
+ [Node.js](https://nodejs.org/) v10.x or greater
  - Verify by running `node -v` and you will see something like `v10.15.1`
  - Make sure we have installed our dependencies in the `mflix-js` directory
    + `cd mflix-js`
    + `npm install`
+ MongoDB setup
  - We will be using the Cluster we created on MongoDB Atlas; however you will need to have the MongoDB server installed and running to have access to `mongorestore` and `mongo`
    + Download MongoDB at [https://www.mongodb.com/download-center/community](https://www.mongodb.com/download-center/community)
+ MongoDB Atlas
  - Create a new user `m220student` with the password `m220password`
  - Go to `Overview -> Connect -> Connect Your Application` and select `Short SRV connection string`
    + You should be able to copy a connection string that allows you to connect via the `mongo` shell
      - `mongo "mongodb+srv://mflix-7um9n.mongodb.net/test" --username m220student`

