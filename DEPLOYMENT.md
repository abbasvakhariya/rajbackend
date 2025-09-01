# Backend Deployment Guide

## Environment Variables Required

Set these environment variables in your Render deployment:

```env
# MongoDB Connection String
MONGO_URI=mongodb+srv://your_username:your_password@your_cluster.mongodb.net/your_database

# Email Configuration (for OTP sending)
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_password

# Server Port
PORT=5000

# Node Environment
NODE_ENV=production
```

## Important Notes for Email Setup

1. **Gmail App Password**: Use an App Password, not your regular Gmail password
2. **Enable 2FA**: You must enable 2-factor authentication on your Gmail account
3. **Generate App Password**: Go to Google Account Settings > Security > App Passwords
4. **Use App Password**: Use the generated 16-character app password in EMAIL_PASS

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
