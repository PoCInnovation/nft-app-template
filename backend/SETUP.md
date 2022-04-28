# Setup

## Setup Starton 

- Go to the register page of the [Starton Website](https://app.starton.io/register) and create an account.
- Get your Starton api key in the Developer Section on the Dashboard and copy it in the variable `STARTON_API_KEY` in the `.env` file at the root of the api project.
- Go to the Wallet section, create a Starton Wallet and claim faucets on the Matic Polygon (Ex Matic) mumbai network with your own wallet address.

## Setup Docker

You need to install Docker and Docker-Compose on your system to launch the database. Here is documentation for it : [Install Docker Engine](https://docs.docker.com/engine/install/), [Install Docker Compose](https://docs.docker.com/compose/install/).

Be careful, after installing docker you will also need to follow this steps: [Manage Docker as a non-root user](https://docs.docker.com/engine/install/linux-postinstall/#manage-docker-as-a-non-root-user), [Configure Docker to start on boot](https://docs.docker.com/engine/install/linux-postinstall/#configure-docker-to-start-on-boot)

## Install Node and Npm

To start the project, you need npm and a node version >= 17.9.0. Here is documentation about it: [How To Install Node.JS On Linux](https://upstack.co/knowledge/how-to-install-node-js-on-linux), [Install npm on Linux](https://linuxconfig.org/install-npm-on-linux)

To manage your node version you can you use nvm (node version manager), here is the github repository : [Node Version Manager](https://github.com/nvm-sh/nvm)


## Start the project

First of all, you need to launch the database (db).

To do that, you just need to use the command:

    npm run db:up

If the database is started correctly, you will be able to access the [mongoDb interface](http://localhost:8081/)

If you want to stop the db you just need to use the command:

    npm run db:down

After that, use this command to install all the nodes dependencies of the project. These dependencies are all the external packages that your project need:

    npm install

Now, you can launch the backend with nodemon (for hot reload) with the command :

    npm run dev

If the backend starts and connects correctly to the db you will see this on your terminal :

    > backend-starton@1.0.0 dev
    > nodemon src/index.ts

    [nodemon] 2.0.15
    [nodemon] to restart at any time, enter `rs`
    [nodemon] watching path(s): *.*
    [nodemon] watching extensions: ts,json
    [nodemon] starting `ts-node src/index.ts`
    server is listening on 3000
    Connected

## Setup Postman

Postman is a very useful tool for testing backend application.
This tool allow you to test your api's endpoints without a frontend.

To download it, go to the [download page](https://www.postman.com/downloads/) on the Postman Website.

After that, click on the import button on your Postamn interface and import the file [StartonApi.postman_collection.json](./Postman/StartonApi.postman_collection.json) this provided you tests for each endpoints.

Congratulations, you can now start the backend project ! 🎉