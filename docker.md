# Docker 

### Prerequisites

- [Docker for Mac](https://docs.docker.com/docker-for-mac/install/)
- [Docker Hub](https://cloud.docker.com)

### Express Starter Code

```
$ npm init
```

```
$ npm i express --save
```

```
$ npm i mongoose --save
```

```
$ npm i nodemon --save
```

```js
// index.js
const express = require('express');
const app = express();

// const mongoose = require('mongoose');
// mongoose.connect('mongodb://mongo:27017');

app.get('/', (req, res) => {
  res.send('Hello, World');
});

app.listen(4000, () => {
  console.log('Example app listening on port 4000');
});
```

## Nodejs + MongoDB

Create our base image 

```Dockerfile
# As of now, the latest runtime supported on AWS Lambda
FROM node:6.10.3

# Create the directory app and dependencies will be installed to
RUN mkdir /app

# Set as application directory in container
WORKDIR /app

# We only want to copy and run this file to optimize caching for Docker, otherwise dependencies could be installed every time a file is changed
COPY package.json /app
RUN npm install

# As one of the last steps, copy the working files over
COPY . /app

EXPOSE 3000

CMD ["npm", "start"]
```

Create the image

```
docker build -t node-test:0.1 .
```

Create a container based on the image

```
docker run -p 3000:3000 -ti node-test:0.1
```

```Dockerfile
# docker-compose.yml
version: "2"
services:
  web:
    # Build image if not already present
    build: .
    # Mount the code so we can work with it like a normal dev environment
    volumes:
      - ./:/app
    # Expose port to the client machine
    ports:
      - "3000:3000"
    # Link services between containers
    links:
      - mongo
  # The ‘mongo’ service name is also added to the /etc/hosts in the container, allowing access to the service as such: mongodb://mongo:27017
  mongo:
    # Use the official MongoDB image
    image: mongo
    ports:
      - "27017:27017"
    # Allow the mongo database container to share the /data/db mounted volume across containers
    volumes_from:
      - mongodata
  # Abstracting the data volume to its own container allows for portability and seperate containers to share the same db
  mongodata:
    image: tianon/true
    volumes:
      - /data/db
```

```
$ docker-compose up
```

#### Adding MongoDB

Uncomment the MongoDB related lines in **index.js**

## Reference

- https://medium.com/@sunnykay/docker-development-workflow-node-express-mongo-4bb3b1f7eb1e
- https://runnable.com/blog/9-common-dockerfile-mistakes
- https://runnable.com/blog/9-common-dockerfile-mistakes
