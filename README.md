# Socket.IO Communication Demo

This project shows how to use Socket.IO for real-time communication between a frontend and a backend.

## Frontend

The frontend is made with React TypeScript and lets you add and remove widgets that subscribe to different topics. The widgets show the messages from the backend for each topic.

The frontend uses a SocketClient class to manage the Socket.IO connection and the subscribed topics. It also reconnects and resubscribes when needed.

The frontend saves messages in sessionStorage and removes old topics when it runs out of space.

## Backend

The backend is made with Python, Flask, and Flask-SocketIO. It has an API for subscribing and unsubscribing to topics with socket.io events. The backend sends a random message for each topic every second to the subscribers.

The backend also has a debugging page that shows the subscribed topics for each session ID.

## Running the Application

### Frontend

1. Go to the `./frontend` directory.
2. Run `npm start` for debug mode or `npm run build && serve -s build` for release mode.
3. The frontend will be at localhost:3000.

Note: The frontend will be in strict mode when running `npm start` and this may cause extra widget remounts and subscription events.

### Backend

1. Go to the `./backend` directory.
2. Run `./main.py`.
3. The backend debugging page will be at localhost:5001.
