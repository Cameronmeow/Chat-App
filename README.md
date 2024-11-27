# ChatHub - Real-time Chat Application

A modern real-time chat application built with Next.js, Node.js, and MongoDB.

## Prerequisites

- Node.js 16.x or later
- MongoDB (local installation or MongoDB Atlas account)
- npm or yarn package manager

## Local Development Setup

1. **Clone the repository**
```bash
git clone <repository-url>
cd chathub
```

2. **Install dependencies**
```bash
npm install
```

3. **Set up environment variables**
```bash
# Copy the example env file
cp .env.example .env
```

Then edit `.env` with your settings:
- `MONGODB_URI`: Your MongoDB connection string
- `JWT_SECRET`: A secure random string for JWT signing
- `FRONTEND_URL`: Keep as http://localhost:3000 for local development
- `PORT`: The port for your backend server (default: 5000)

4. **Start MongoDB**
- If using local MongoDB:
  ```bash
  mongod
  ```
- If using MongoDB Atlas:
  - Create a cluster
  - Get your connection string
  - Update MONGODB_URI in .env

5. **Start the development servers**

In one terminal, start the backend:
```bash
npm run server
```

In another terminal, start the frontend:
```bash
npm run dev
```

## Available Scripts

- `npm run dev`: Start the Next.js development server
- `npm run server`: Start the backend API server
- `npm run build`: Build the Next.js application
- `npm start`: Start the production server
- `npm run lint`: Run ESLint

## Features

- Real-time messaging
- User authentication
- Group chat functionality
- Video and audio calling
- Message history
- Online presence indicators

## Architecture

- Frontend: Next.js 13 with App Router
- Backend: Node.js with Express
- Database: MongoDB with Mongoose
- Real-time: Socket.IO
- Video Calling: WebRTC with simple-peer

## API Routes

### Authentication
- POST `/api/auth/register` - Register a new user
- POST `/api/auth/login` - Login user

### Messages
- GET `/api/messages/channel/:channelId` - Get channel messages
- POST `/api/messages` - Send a message

### Channels
- GET `/api/channels` - Get user's channels
- POST `/api/channels` - Create a new channel
- POST `/api/channels/:channelId/join` - Join a channel
- POST `/api/channels/:channelId/leave` - Leave a channel# Chat-App
