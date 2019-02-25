Homework: Full Stack Games Hub App
Learning Objectives
Understand the relationship between client, server and database
Be able to navigate a codebase that you haven't written
Brief
Your boss has asked to you look over the codebase of a full-stack JavaScript application. The front-end is written in JavaScript using Vue, the back-end uses an Express server and a MongoDB database. Your task is to make yourself familiar with the codebase.

The application includes a README.md with instructions on running the application.

Overview of the tech stack and tooling with commands

MVP
Task
Draw a diagram showing the dataflow through the application starting with a form submission, ending with the re-rendering of the page. This will involve a multi-direction data-flow with the client posting data to the server and the server sending data back to the client with the response. Detail the client, server and database in the diagram and include the names of the files involved in the process.

Questions
What is responsible for defining the routes of the games resource?
```
The router is responsible for defining the routes of the games resource.
```
What do you notice about the folder structure? Whats the client responsible for? Whats the server responsible for?
```
The client is responsible for the front-end JavaScript Vue framework. The server is responsible for listening out for requests being made and responds to them.
```
What are the the responsibilities of server.js?
```
server.js is responsible for importing (or 'requiring' in) additional nodes, listening to the port and passing route requests through to the router.
```
What are the responsibilities of the gamesRouter?
```
The router parses in a collection of data from server.js, and depending on the request it processes the request, updating the MongoDB (and in turn the API) and returning a response in json format.
```
What process does the the client (front-end) use to communicate with the server?
```
The client is responsible for emiting requests to the server and then retrieving (or 'fetching') the response from the API.
```
What optional second argument does the fetch method take? And what is it used for in this application? Hint: See Using Fetch on the MDN docs
```
The fetch method can take an 'init options object' as a second argument. This second argument allows you to pass in a method type (e.g. GET, POST), converts the json payload into a string (for passing through to the server), and provides headers. In GameForm.vue it is used to parse through the data submitted by the form to the server.
```
Which of the games API routes does the front-end application consume (i.e. make requests to)?
```
http://localhost:3000/api/games
```
What are we using the MongoDB Driver for?
```
The MongoDB Driver communicates between the database at the server. It is also responsible for updating the server and making requests to the DB.
```
Extension
Why do we need to use ObjectId from the MongoDB driver?
```
ObjectId helps us to identify object id values from the database.
```
Add to your diagram the dataflow for removing a game.
