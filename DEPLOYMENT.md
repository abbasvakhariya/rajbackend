# Backend Deployment Guide

## Environment Variables Required

Create a `.env` file in the backend directory with the following variables:

```env
# MongoDB Connection String
MONGO_URI=mongodb://localhost:27017/your_database_name

# Email Configuration (for OTP sending)
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_password

# Server Port
PORT=5000

# Node Environment
NODE_ENV=production
```

## Deployment Steps

1. **Install Dependencies:**
   ```bash
   npm install
   ```

2. **Build the Application:**
   ```bash
   npm run build
   ```

3. **Start the Server:**
   ```bash
   npm start
   ```

## Available Scripts

- `npm start` - Start the production server
- `npm run dev` - Start development server with nodemon
- `npm run build` - Build the application
- `npm test` - Run tests

## API Endpoints

- `POST /api/request-otp` - Request OTP for login/register
- `POST /api/verify-otp` - Verify OTP
- `POST /api/forgot-password` - Send OTP for password reset
- `POST /api/reset-password` - Reset password with OTP

## Notes

- Make sure MongoDB is running and accessible
- Configure email settings for OTP functionality
- Set appropriate CORS settings for your frontend domain
