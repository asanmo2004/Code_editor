# Pair Code: Realtime Collaborative Code Editor

## Introduction

Are you tired of sending code snippets back and forth, struggling to debug and collaborate with your team? Look no further! **Pair Code** is here to revolutionize the way you code together. This powerful and intuitive collaborative code editor is designed to empower developers, and teams to work seamlessly in real-time, regardless of their location. With **Pair Code**, you can code together, debug together, and ship faster, together.

## Features

- Multiple users can join a room and edit code together
- Changes are reflected in real time
- Copy button to copy the room id to clipboard
- Leave button to leave the room
- Supports syntax highlighting for different programming languages
- Users can choose theme based on their preferences
- Users can leave the room and rejoin later to continue editing
- Joining & leaving of users is also reflected in real time

Explore PairCode: https://mypaircode.vercel.app/
### Prerequisites

#### For running via Docker

- Docker (25.0.4)
- Docker Compose (1.29.2)

#### For running locally

- Node.js (v20.11.1)
- npm (10.2.4)
- pm2 (5.3.1) : run `npm i -g pm2` to install pm2 globally

**Note:** I have used nvm (v0.39.7) to manage my node versions. View nvm official [documentation](https://github.com/nvm-sh/nvm) to install it.

## Tech Stack

- React.js
- Node.js
- Express.js
- Socket.io
- CodeMirror
- React-Toastify

## Installation

### Running via Docker Image (highly recommended)

To run the docker image, follow the steps below:

1. Install [Docker](https://www.docker.com/) on your machine.
2. Pull the docker image from the docker hub by running `docker pull asan10/code-editor`
3. Run the docker image by running `docker run -p 8000:8000 -p 3000:3000 -p 5000:5000 asan10/code-editor`
4. Go to `http://localhost:3000` to view the app
5. Create a room by clicking on the `create new room` button and put a username of your choice
   5 . Copy the room id by clicking on the `Copy ROOM ID` button
6. To join as an another user open another browser/browser-window or an incognito tab and go to `http://localhost:3000`
7. Enter the same room id to join the same room

Now both your editor will be synced and you can see the changes in real time. Try opening the same room in multiple browsers/browsers-windows and see the changes.

**Note:** If you are using docker in wsl2/linux then add `sudo` before the docker commands.

### Running via building your own Docker Image

To run the app using docker, follow the steps below:

1. Install [Docker](https://www.docker.com/) on your machine.
2. Clone the project repository and Navigate to the project directory.
3. Also you have to change ENV values in the Dockerfile
4. Replace your username in docker-compose.yml file.
5. Run the Docker Compose command: `docker-compose up -d`
6. Go to `http://localhost:3000` to view the app
7. Follow the steps 5-7 from the [Running via Docker Image](https://github.com/Mohitur669/Realtime-Collaborative-Code-Editor?tab=readme-ov-file#running-via-docker-image) section to create and join a room

### Running Locally

1. Clone this repository and cd into it
2. Run `npm install` to install the dependencies
3. Create .env file in the root folder and copy paste the content of example.env, and add necessary credentials.
4. To start the react app client run `npm start` in one terminal
5. To start the server run `npm server:dev` or `pm2 start server.js` in another terminal
6. Go to `http://localhost:3000` to view the app
7. Follow the steps 4-7 from the [Running via Docker Image](https://github.com/Mohitur669/Realtime-Collaborative-Code-Editor?tab=readme-ov-file#running-via-docker-image) section to create and join a room

**Note:** To stop your server, press `Ctrl+c` or if you used "pm2", then use `pm2 stop server.js` in the terminal.

