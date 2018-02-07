# Docker w/ Nodejs + Express

### Prerequisites

- [Docker for Mac](https://docs.docker.com/docker-for-mac/install/)
- [Docker Hub](https://cloud.docker.com)

### Express Starter Code

```
$ npm init
```

> Note: Docker will fail if there's no start script
> 
> "start": "node index.js"

```
$ npm i express nodemon --save
```

```js
// index.js
const express = require('express');
const app = express();

app.get('/', (req, res) => {
  res.send('Hello, World');
});

app.listen(8080, () => {
  console.log('Example app listening on port 8080');
});
```

## Nodejs

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

EXPOSE 8080

# Example, only include env vars as needed to optimize the cache, place at bottom if Dockerfile doesn't need it to build the image
#ENV NODE_ENV development

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

## Reference

- https://medium.com/@sunnykay/docker-development-workflow-node-express-mongo-4bb3b1f7eb1e
- https://runnable.com/blog/9-common-dockerfile-mistakes
- https://runnable.com/blog/9-common-dockerfile-mistakes
