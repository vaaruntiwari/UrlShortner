# URL Shortener

A URL shortening application built with **Express.js** and **React.js**. It provides a web interface for creating short links and an Express API for managing and redirecting them.

## Tech stack

- **Frontend:** React.js
- **Backend:** Node.js and Express.js

## Getting started

### Prerequisites

- Node.js (LTS recommended)
- npm

### Install dependencies

Install the dependencies in the frontend and backend directories (adjust the paths to match your project layout):

```bash
cd backend
npm install

cd ../frontend
npm install
```

### Run the application

Open separate terminals and start the backend and frontend using the scripts defined in each directory's `package.json`:

```bash
# Terminal 1
cd backend
npm run dev

# Terminal 2
cd frontend
npm start
```

If your project uses different directory names or start scripts, use the corresponding paths and commands from its `package.json` files.

## Configuration

Put environment-specific settings in a `.env` file in the relevant application directory. Keep secrets and local configuration out of version control. The required variable names depend on the services configured by the backend.

## Project structure

The project separates the React client from the Express server. A typical layout is:

```text
.
|-- backend/     # Express API and redirect handling
`-- frontend/    # React user interface
```

## Development notes

- Start the Express server and React development server independently during local development.
- Configure the client to send API requests to the backend's local address.
- Add production build and deployment instructions once the hosting setup is chosen.
