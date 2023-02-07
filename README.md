## Persist data with Docker Volumes

This app shows a simple user profile app set up using

- index.html with pure js and css styles
- nodejs backend with express module
- mongodb for data storage

All components are docker-based

### Technologies used:

Docker compose, Node.js,HTML, CSS, JavaScript, MongoDB, MongoExpress

### Project Description:

1- Create docker volumes in Docker-compose file

2- Persist data of a MongoDB container by attaching a Docker volume to it

3- Start our application container with MongoDB and MongoExpress services using docker compose

### With Docker compose

#### To start the application

Step 1: Add volumes to mongodb to persist data

![Alt text](app/images/compose-yaml.png?raw=true)

Step 2: Run mongodb, mongo-express containers by docker compose on remote server

    docker compose up

or

    docker compose -f docker-compose.yaml up

Step 3: mongodb, mongo-express are running

mongodb: listening on port 27017

mongo-express: listening on prot 8081

![Alt text](app/images/Screenshot%202023-02-07%20at%2010.25.54%20pm.png?raw=true)

Step 3: open mongo-express on browser via port 8081

1-Create a new database: my-app

2-Create a new collection inside my-app database: users

Step 4: run app locally

    cd ./app

    npm install

    npm run start

Step 5: edit the user profile

![Alt text](app/images/Screenshot%202023-02-07%20at%206.56.15%20pm.png?raw=true)

![Alt text](app/images/Screenshot%202023-02-07%20at%206.56.57%20pm.png?raw=true)
Step 8: Stop the node app

    docker compose down

or

    docker compose -f docker-compose.yaml down

Step 9: Re-start the mongodb, mongo-express and node app

    docker compose up

    cd ./app

    npm run start
