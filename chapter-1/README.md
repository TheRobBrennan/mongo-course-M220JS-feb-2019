# Welcome
Chapter 1 focuses on getting the mflix application up and running on your local development machine. Once the initial setup is complete, I would love to Dockerize this project so that it can run in its own containerized process for development.

## Initial setup
The easiest way to use this repo is to have [Docker](https://www.docker.com) installed and configured on your development machine.

Make sure that you have the following setup and configured
+ [Node.js](https://nodejs.org/) v10.x or greater
  - Verify by running `node -v` and you will see something like `v10.15.1`
  - Make sure we have installed our dependencies in the `mflix-js` directory
+ MongoDB setup
  - We will be using the Cluster we created on MongoDB Atlas; however you will need to have the MongoDB server installed and running to have access to `mongorestore` and `mongo`
    + Download MongoDB at [https://www.mongodb.com/download-center/community](https://www.mongodb.com/download-center/community)
+ MongoDB Atlas
  - Create a new user `m220student` with the password `m220password`
  - Go to `Overview -> Connect -> Connect Your Application` and select `Short SRV connection string`
    + You should be able to copy a connection string that allows you to connect via the `mongo` shell
      - `mongo "mongodb+srv://mflix-7um9n.mongodb.net/test" --username m220student`

If you have installed Docker on your system, you should be able to run `npm run docker:up` to spin up the required application and database containers.

This guide assumes you have an ability to connect to the MongoDB container that is running when executing any `mongorestore` or `mongo` commands.

### Import example data
To import the example data, please use your favorite tool to connect to your MongoDB instance. In my case, I am using VS Code with the Docker extension.

From the root level of your MongoDB container, you should be able to import data as:
```sh
> mongorestore --drop --gzip --db test --uri "mongodb+srv://m220student:m220password@mflix-7um9n.mongodb.net/test" mflix
```

Once your data has imported successfully, you can then update the user credentials to have a different username and password. Refer to `mflix-js/README.md` for information on creating your local `mflix-js.env` file.

After you have completed that, you can start your project with:
```
// Spin up the Docker containers
$ npm run docker:up:clean
// Do some stuff
// Spin down the Docker containers
$ npm run docker:down
```

Alternatively, there is a short cut to starting/stopping your project:
```
$ npm run docker:refresh:clean          // Builds a fresh Docker infrastructure
$ npm run docker:refresh                // Refresh your environment
```

One cool thing about having this application Dockerized is that any changes you make will be instantly reloaded.

Your application should be available at [http://localhost:5000](http://localhost:5000).

## Ticket: Projection
Modify `getMoviesByCountry` in `mflix-js/src/dao/moviesDAO.js` so that `mflix-js/test/projection.test.js` passes. Verify by running:
```
$ npm test -t projection
```
