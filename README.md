# Personal Finance Tracker

A full-stack web application for tracking personal income and expenses with AI-powered budget insights.

## Tech Stack

- **Frontend**: React, Recharts, Axios
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **AI**: Google Gemini API

## Prerequisites

- Node.js (v14+)
- MongoDB Atlas account (or local MongoDB)
- Google Gemini API key

## Setup

### 1. Clone the repository
```bash
git clone <repository-url>
cd repository-name
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
MONGODB_URI=mongodb+srv://username:password@cluster0.xxxxx.mongodb.net/finance-tracker?retryWrites=true&w=majority
JWT_SECRET=your_super_secret_jwt_key_here_make_it_long_and_secure
GEMINI_API_KEY=your-gemini-api-key
PORT=5050
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
REACT_APP_API_URL=http://localhost:5050/api
```

### 4. MongoDB Atlas Setup
- Create a MongoDB Atlas account at https://cloud.mongodb.com
- Create a new cluster and get your connection string
- Replace `username`, `password`, and cluster URL in the MONGODB_URI

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
- Backend API: `http://localhost:5050`

## Demo Account

For testing purposes, you can use the following demo account:
- **Email**: demo@gmail.com
- **Password**: demo
- **Name**: demo
## 🚀 Live Demo
**Deployed Application**: https://finance-app-5-1.onrender.com

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
- Mobile responsive
- Fully Deployed
- JWT Authentication

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
- `PORT` - Server port (default: 5050)

### Frontend (client/.env)
- `REACT_APP_API_URL` - Backend API URL