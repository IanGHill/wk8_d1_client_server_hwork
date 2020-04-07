### Questions

1. What is responsible for defining the routes of the `games` resource?

In this context I'm assuming the 'games resourse' means the games API? In which case the create_router.js defines the routes.

2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?
3. 
Client and Server code live in two completely separate folders. Client is responsible for front-end, displaying content to user via browser. Client sends requests to and receives responses from the server. Server receives requests from client, processes them, handles communications with the database and sends back information to client.

3. What are the the responsibilities of server.js?

Setting up connection with database. Utilising middleware. Listening for incoming requests on port 3000.
 
4. What are the responsibilities of the `gamesRouter`?

Setting up route between incoming requests and the DB?

5. What process does the the client (front-end) use to communicate with the server?

Sends fetch requests using URL & restful routes

6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs

An init object that allows you to control some settings.

7. Which of the games API routes does the front-end application consume (i.e. make requests to)?

Get in order to display something? With the other routes the front-end is sending requests for the back-end to do something (e.g. alter the database)

8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?

To allow our application to communicate with the database - retrieving and updating data.

## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?

To provide a unique reference to the database.

Add to your diagram the dataflow for removing a game.