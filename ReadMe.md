# Microservices 
This project is a sample implementation of microservices using node js. There are two types of communications among services in microservice architecture, Sync and Async.
In Sync communication services communicate directly to other services or their databases. This creates huge dependency and if any service goes down it will take down everything dependant on it. Or if database model is updated you will need to update the service as well.
In Async communication you create an event bus in which events are saved and they are called on other services. This approach asks for data duplication if required.

### Usage
#### Client App
React app which is using backend microservices to create and display the comments and posts.
Run     'npm install' to install dependencies
Run     'npm start' to execute app.

#### Comments
Node js Microservice used to create comments and handle comment creation events for event bus.
Run     'npm install' to install dependencies
Run     'npm start' to execute app.

#### Posts
Node js Microservice used to create posts and handle post creation events for event bus.
Run     'npm install' to install dependencies
Run     'npm start' to execute app.

#### Query
Node js Microservice used to call only one request to get all posts with all comments on them. This gets data from both Posts and Comment microservice using event bus.
Run     'npm install' to install dependencies
Run     'npm start' to execute app.

#### Event Bus
Node js Microservice used to register and dispatch events on all microservices.
Run     'npm install' to install dependencies
Run     'npm start' to execute app.

