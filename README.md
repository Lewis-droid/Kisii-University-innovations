# Kisii University Marks Management System

A futuristic, AI-powered platform designed to solve the problem of incomplete or missing student marks at Kisii University.

## Overview

The Kisii University Marks Management System is a comprehensive web application that enables students to track their academic records in real-time, report issues with missing or incomplete marks, and get instant answers to academic questions through an AI chatbot. Lecturers benefit from an admin dashboard to efficiently manage and respond to student queries.

## Features

### For Students
- **Real-time Academic Records**: Check your grades and academic progress instantly
- **Ticket Management System**: Raise tickets for:
  - Missing marks (Grade "I")
  - Incomplete marks
  - Remark requests
- **AI Chatbot Assistant**: Get immediate answers to academic questions
- **Notification System**: Receive email/SMS alerts for ticket status updates
- **Secure Document Upload**: Submit supporting documents for your cases

### For Lecturers/Administrators
- **Admin Dashboard**: Manage student complaints and track resolution progress
- **Ticket Management**: View, prioritize, and respond to student requests
- **Analytics**: Track common issues and response metrics
- **Notification System**: Stay updated on urgent student requests

### System Features
- **Role-based Access Control**: Secure login system for students and staff
- **Mobile-responsive Design**: Optimized for all device sizes
- **Modern UI/UX**: Futuristic blue and black interface with smooth animations
- **University Calendar Integration**: Important deadlines and dates
- **FAQ Section**: AI-powered frequently asked questions

## Technology Stack

### Frontend
- React.js with hooks for state management
- TailwindCSS for styling
- Framer Motion for animations
- Axios for API communication

### Backend
- Node.js with Express.js
- MongoDB with Mongoose ODM
- JWT for authentication
- Socket.io for real-time notifications

### AI Components
- Python with TensorFlow/NLP libraries
- Custom-trained model for academic queries
- Integration with university knowledge base

### Additional Services
- Firebase for file storage
- Twilio for SMS notifications
- Nodemailer for email services

## Installation

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (v4.4 or higher)
- Python (v3.8 or higher) for AI components
- npm or yarn

### Setup Instructions

1. Clone the repository:
```bash
git clone https://github.com/kisii-university/marks-management-system.git
cd marks-management-system
```

2. Install backend dependencies:
```bash
cd backend
npm install
```

3. Install frontend dependencies:
```bash
cd ../frontend
npm install
```

4. Set up environment variables:
Create a `.env` file in the backend directory with:
```
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
EMAIL_SERVICE=your_email_service
EMAIL_USER=your_email_address
EMAIL_PASS=your_email_password
TWILIO_ACCOUNT_SID=your_twilio_sid
TWILIO_AUTH_TOKEN=your_twilio_token
```

5. Set up AI service:
```bash
cd ../ai-service
pip install -r requirements.txt
```

6. Start the development servers:
```bash
# Terminal 1 - Start backend
cd backend
npm run dev

# Terminal 2 - Start frontend
cd frontend
npm start

# Terminal 3 - Start AI service (if needed)
cd ai-service
python app.py
```

## Usage

### For Students
1. Log in with your student credentials
2. View your academic dashboard with current grades
3. Report missing marks using the ticket system
4. Chat with the AI assistant for academic guidance
5. Receive notifications when your issues are resolved

### For Lecturers
1. Log in with staff credentials
2. Access the admin dashboard
3. View and manage student tickets
4. Update student records as needed
5. Monitor common issues through analytics

## API Documentation

The API endpoints are organized as follows:

### Authentication
- `POST /api/auth/login` - User login
- `POST /api/auth/register` - User registration
- `GET /api/auth/verify` - Verify JWT token

### Tickets
- `GET /api/tickets` - Get all tickets (with filters)
- `POST /api/tickets` - Create a new ticket
- `GET /api/tickets/:id` - Get specific ticket
- `PUT /api/tickets/:id` - Update ticket status
- `DELETE /api/tickets/:id` - Delete ticket

### Academic Records
- `GET /api/records/:studentId` - Get student records
- `POST /api/records` - Add new record (admin only)
- `PUT /api/records/:id` - Update record (admin only)

### AI Chatbot
- `POST /api/chat` - Send message to chatbot
- `GET /api/chat/history` - Get chat history

## Deployment

### Production Build
```bash
# Build frontend
cd frontend
npm run build

# Start production server
cd ../backend
npm start
```

### Docker Deployment
Dockerfiles are provided for containerized deployment:
```bash
docker-compose up --build
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support or questions about this system:
- Email: support@kisiiuniversity.ac.ke
- Issue Tracker: https://github.com/kisii-university/marks-management-system/issues

## Acknowledgments

- Kisii University IT Department
- University Administration
- Student representatives for feedback and testing

---

**Note**: This system is designed for Kisii University and integrates with existing university systems. Proper authorization is required for access to student data.
