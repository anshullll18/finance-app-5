# Personal Finance Tracker

A full-stack web application for tracking personal income and expenses with AI-powered budget insights.

## Tech Stack

- **Frontend**: React, Recharts, Axios
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **AI**: Google Gemini API

## Prerequisites

- Node.js (v14+)
- MongoDB (local or Atlas)
- Google Gemini API key

## Setup

### 1. Clone the repository
```bash
git clone <repository-url>
cd finance-tracker
```

### 2. Backend Setup
```bash
# Install server dependencies
npm install

# Create .env file in root directory
touch .env
```

Add the following to `.env`:
```env
MONGODB_URI=mongodb://127.0.0.1:27017/finance-tracker
JWT_SECRET=your-jwt-secret-key
GEMINI_API_KEY=your-gemini-api-key
PORT=5000
```

### 3. Frontend Setup
```bash
# Navigate to client directory
cd client

# Install client dependencies
npm install

# Create .env file in client directory
touch .env
```

Add the following to `client/.env`:
```env
REACT_APP_API_URL=http://localhost:5000/api
```

### 4. Start MongoDB
```bash
# If using local MongoDB
mongod
```

### 5. Run the Application

**Terminal 1 - Backend:**
```bash
# From root directory
npm start
```

**Terminal 2 - Frontend:**
```bash
# From client directory
cd client
npm start
```

The application will be available at:
- Frontend: `http://localhost:3000`
- Backend API: `http://localhost:5000`

## Features

- User authentication (register/login)
- Add, edit, delete transactions
- Categorize income and expenses
- View spending by category (pie chart)
- Monthly statistics
- Date range filtering
- CSV export
- AI budget insights
- Dark/light mode

## API Endpoints

- `POST /api/register` - User registration
- `POST /api/login` - User login
- `GET /api/transactions` - Get user transactions
- `POST /api/transactions` - Create transaction
- `PATCH /api/transactions/:id` - Update transaction
- `DELETE /api/transactions/:id` - Delete transaction
- `GET /api/stats` - Get dashboard statistics
- `GET /api/monthly-stats` - Get monthly statistics
- `POST /api/ai-insight` - Get AI budget insight

## Environment Variables

### Backend (.env)
- `MONGODB_URI` - MongoDB connection string
- `JWT_SECRET` - Secret key for JWT tokens
- `GEMINI_API_KEY` - Google Gemini API key
- `PORT` - Server port (default: 5000)

### Frontend (client/.env)
- `REACT_APP_API_URL` - Backend API URL