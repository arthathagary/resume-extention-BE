# Resume Extension BE

This is a basic Express.js backend project implementing JWT authentication (signup, login, protected routes).

## Prerequisites

- Node.js v14+ installed

## Setup

1. Install dependencies:
   ```bash
   npm install
   ```
2. Create a `.env` file in the project root with:
   ```env
   JWT_SECRET=your_jwt_secret
   PORT=5000 # optional
   ```

## Available Scripts

- `npm start` - Run the server
- `npm run dev` - Run the server with nodemon for development

## API Endpoints

### Signup

- URL: `POST /api/auth/signup`
- Body:
  ```json
  { "username": "user1", "password": "pass123" }
  ```

### Login

- URL: `POST /api/auth/login`
- Body:
  ```json
  { "username": "user1", "password": "pass123" }
  ```
- Response:
  ```json
  { "token": "<jwt_token>" }
  ```

### Protected Route Example

- URL: `GET /api/protected`
- Header:
  ```http
  Authorization: Bearer <jwt_token>
  ```
- Response:
  ```json
  { "message": "Hello user1, you are authorized." }
  ```

## Debugging in VS Code

1. Open the Debug view in VS Code (Ctrl+Shift+D or Cmd+Shift+D).
2. Create a new launch configuration and select **Node.js**.
3. Use the default configuration, setting `program` to `${workspaceFolder}/index.js`.
4. Start the debugger.
