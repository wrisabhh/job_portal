# JobPortal - MERN Stack Job Portal with Cloudinary Integration

## Overview

JobPortal is a modern job search platform built using the MERN stack (MongoDB, Express.js, React.js, Node.js) with Cloudinary integration for image storage. This application allows job seekers to browse and apply for jobs while enabling employers to post job openings.

## Features

- **User Authentication**: Secure login/signup for both job seekers and employers
- **Job Listings**: Browse and search for available jobs
- **Job Posting**: Employers can create and manage job postings
- **Responsive Design**: Mobile-friendly interface
- **Cloudinary Integration**: For storing company logos and user profile pictures
- **Job Categories**: Filter jobs by category (Frontend, Backend, etc.)

## Technologies Used

### Frontend
- React.js
- Redux (for state management)
- Axios (for API calls)
- React Router (for navigation)
- Tailwind CSS (for styling)

### Backend
- Node.js
- Express.js
- MongoDB (with Mongoose ODM)
- JSON Web Tokens (for authentication)
- Cloudinary SDK (for image uploads)

### Deployment
- Vercel/Netlify (for frontend)
- Render/Heroku (for backend)
- MongoDB Atlas (for database)
- Cloudinary (for media storage)

## Setup Instructions

### Prerequisites
- Node.js (v14 or later)
- MongoDB Atlas account
- Cloudinary account
- Git

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/jobportal-mern.git
   cd jobportal-mern
   ```

2. Install dependencies for both client and server:
   ```bash
   # Install server dependencies
   cd server
   npm install

   # Install client dependencies
   cd ../client
   npm install
   ```

3. Create a `.env` file in the server directory with the following variables:
   ```
   MONGO_URI=your_mongodb_atlas_connection_string
   JWT_SECRET=your_jwt_secret_key
   CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
   CLOUDINARY_API_KEY=your_cloudinary_api_key
   CLOUDINARY_API_SECRET=your_cloudinary_api_secret
   ```

4. Start the development servers:
   ```bash
   # From the project root directory
   cd server
   npm run dev & cd ../client && npm start
   ```

## Project Structure

```
jobportal-mern/
├── client/               # Frontend React application
│   ├── public/           # Static files
│   └── src/              # React components, pages, etc.
│       ├── components/   # Reusable components
│       ├── pages/        # Application pages
│       ├── redux/        # Redux store and slices
│       └── App.js        # Main application component
│
├── server/               # Backend Express application
│   ├── config/           # Configuration files
│   ├── controllers/      # Route controllers
│   ├── middleware/       # Custom middleware
│   ├── models/           # MongoDB models
│   ├── routes/           # API routes
│   ├── utils/            # Utility functions
│   └── server.js         # Main server file
│
├── .gitignore            # Files to ignore in version control
└── README.md             # This file
```

## API Endpoints

| Endpoint                | Method | Description                          |
|-------------------------|--------|--------------------------------------|
| /api/auth/register      | POST   | Register a new user                  |
| /api/auth/login         | POST   | Login user                           |
| /api/jobs               | GET    | Get all jobs                         |
| /api/jobs               | POST   | Create a new job (employer only)     |
| /api/jobs/:id           | GET    | Get job details                      |
| /api/jobs/:id           | PUT    | Update job (employer only)           |
| /api/jobs/:id           | DELETE | Delete job (employer only)           |
| /api/jobs/:id/apply     | POST   | Apply for a job (job seeker only)    |
| /api/users/profile      | GET    | Get user profile                     |
| /api/users/profile      | PUT    | Update user profile                  |
| /api/upload             | POST   | Upload image to Cloudinary           |

## Deployment

### Frontend Deployment (Vercel/Netlify)
1. Push your code to a GitHub repository
2. Connect the repository to your Vercel/Netlify account
3. Set environment variables if needed
4. Deploy!

### Backend Deployment (Render/Heroku)
1. Create a new web service on Render or Heroku
2. Connect your GitHub repository
3. Add environment variables (same as your .env file)
4. Deploy!

### Database Deployment
- Use MongoDB Atlas for cloud database hosting
- Whitelist your IP addresses and application URLs


## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License

This project is licensed under the MIT License.

## Contact

For questions or support, please contact [yadavrishabh1410@gmail.com].
