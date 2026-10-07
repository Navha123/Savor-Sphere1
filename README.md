# SavorSphere - Recipe Management System

A comprehensive MERN stack web application for recipe management, discovery, and sharing.

## Features

### User Features
- User authentication (login/signup)
- Create, edit, and delete recipes
- Browse and search recipes
- Bookmark favorite recipes
- Personal dashboard with statistics
- To-do list and task management
- Activity tracking
- Generate and download reports

### Admin Features
- User management
- Recipe approval system
- Category management
- Analytics and reports
- System settings

## Tech Stack

### Frontend
- React.js
- Redux Toolkit
- React Router
- Tailwind CSS
- Axios
- React Toastify

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT Authentication
- Bcrypt for password hashing
- Nodemailer for emails

## Installation

### Prerequisites
- Node.js (v14 or higher)
- MongoDB
- npm or yarn

### Backend Setup
1. Navigate to the server directory:
   ```bash
   cd server
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file with the following variables:
   ```
   NODE_ENV=development
   PORT=5000
   MONGO_URI=mongodb://localhost:27017/savorsphere
   JWT_SECRET=your_jwt_secret_key_here
   EMAIL_HOST=smtp.gmail.com
   EMAIL_PORT=587
   EMAIL_USER=your_email@gmail.com
   EMAIL_PASS=your_email_password
   ```

4. Start the server:
   ```bash
   npm run dev
   ```

### Frontend Setup
1. Navigate to the client directory:
   ```bash
   cd client
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

## Usage

1. Start MongoDB service
2. Run the backend server: `cd server && npm run dev`
3. Run the frontend: `cd client && npm run dev`
4. Open your browser and navigate to `http://localhost:5173`

## Project Structure

```
SavorSphere/
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/     # Reusable components
│   │   ├── pages/          # Page components
│   │   ├── services/       # API services
│   │   ├── store/          # Redux store and slices
│   │   └── styles/         # CSS files
│   └── package.json
├── server/                 # Backend Node.js application
│   ├── config/            # Database configuration
│   ├── controllers/       # Route controllers
│   ├── middleware/        # Custom middleware
│   ├── models/           # MongoDB models
│   ├── routes/           # API routes
│   ├── utils/            # Utility functions
│   └── package.json
└── README.md
```

## API Endpoints

### Authentication
- POST `/api/auth/register` - Register new user
- POST `/api/auth/login` - User login

### Users
- GET `/api/users/profile` - Get user profile
- PUT `/api/users/profile` - Update user profile
- GET `/api/users` - Get all users (admin only)

### Recipes
- GET `/api/recipes` - Get all approved recipes
- POST `/api/recipes` - Create new recipe
- GET `/api/recipes/:id` - Get recipe by ID
- PUT `/api/recipes/:id` - Update recipe
- DELETE `/api/recipes/:id` - Delete recipe

### Categories
- GET `/api/categories` - Get all categories
- POST `/api/categories` - Create category (admin only)
- PUT `/api/categories/:id` - Update category (admin only)
- DELETE `/api/categories/:id` - Delete category (admin only)

### Tasks
- GET `/api/tasks` - Get user tasks
- POST `/api/tasks` - Create new task
- PUT `/api/tasks/:id` - Update task
- DELETE `/api/tasks/:id` - Delete task

### Reports
- GET `/api/reports/generate` - Generate user report
- GET `/api/reports` - Get user reports

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License.