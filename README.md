# Realtime Whiteboard

Realtime Whiteboard is a collaborative online whiteboard application where multiple users can join a room and draw on the whiteboard simultaneously. It includes features like writing on the whiteboard, undoing the last stroke, changing font size and color, saving the canvas as an image, and user authentication using Keycloak.

## Features

- Writing on the whiteboard using pencil or rectangle elements
- Undo last stroke
- Change font size
- Change font color
- Save the canvas as an image
- User authentication, Single Sign-On (SSO), and Identity and Access Management (IAM) using Keycloak
- Create a room
- Multiple people can join a room and write on the whiteboard using web sockets
- Responsive design

## Get Started

1. Clone the repository:
```bash
git clone https://github.com/coderSomya/Realtime-whiteboard.git
cd realtime-whiteboard
```



2. Environment variables setup

Add a `.env` file in the `/auth` directory:

```bash
VITE_KEYCLOAK_URL="http://127.0.0.1:4000"
VITE_KEYCLOAK_REALM=<your_keycloak_realm>
VITE_KEYCLOAK_CLIENT_ID=<your_keycloak_client_id>
VITE_WHITEBOARD_URL="http://localhost:5173"
```

3. Start the server

```bash
npm i
npm run dev
```

4. Start the client
```bash
cd frontend
npm i
npm run dev
```

5. Spin up Keycloak on a Docker container
```bash
docker run -d -p 4000:8080 -e KEYCLOAK_ADMIN=admin -e KEYCLOAK_ADMIN_PASSWORD=admin quay.io/keycloak/keycloak:20.0.3 start-dev
```

## Keycloak Setup

1. Open http://localhost:4000
2. Create a new realm and give it a name
3. Create a new client and give it a name
4. In the client settings, add the web origin as http://localhost:5174
5. Add other settings like user registration, max/min password lengths, etc.

## Technologies Used

- ReactJS
- Typescript
- JavaScript
- NodeJS
- Web sockets
- Keycloak
- Docker

