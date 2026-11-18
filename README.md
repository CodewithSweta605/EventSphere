# EventSphere – Full-Stack Event Booking Platform

EventSphere is a full-stack event booking and management platform built using the MERN stack. It allows users to browse available events, register for events, submit ticket booking requests, and track their booking status. Administrators can create and manage events, review booking requests, and update payment status.

## Features

### 1. User Authentication
- User registration and login.
- JWT-based authentication.
- Password hashing using bcrypt.
- Email OTP verification during registration and booking.

### 2. Event Management
- Browse available events.
- View event details, including descriptions, dates, categories, and seating capacity.
- Admin can create, edit, and delete events.
- Support for free and paid events.

### 3. Ticket Booking
- Submit ticket booking requests through email OTP verification.
- Booking requests are initially marked as pending.
- Users can view their booking status through their dashboard.
- Users can cancel their bookings.
- Seat availability is checked to prevent overbooking.

### 4. Admin Dashboard
- View and manage booking requests.
- Approve or reject booking requests.
- Update payment status as Paid or Not Paid.
- Monitor pending requests, confirmed bookings, and revenue.

### 5. Email Notifications
- Email OTP verification.
- Email notifications after successful booking confirmation.

## Technology Stack

| Category | Technologies |
|---|---|
| Frontend | React.js, Tailwind CSS |
| Backend | Node.js, Express.js |
| Database | MongoDB, Mongoose |
| Authentication | JWT, bcrypt |
| Email Service | Nodemailer |
| Development Tools | Git, GitHub, Postman |

## Project Structure

```text
EventSphere/
│
├── client/                 # React frontend
│   ├── src/
│   ├── public/
│   └── package.json
│
├── server/                 # Node.js and Express backend
│   ├── config/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   └── package.json
│
├── package.json
└── README.md
```

*Note: The folder structure above is a general overview. Update it to match the actual repository.*

## Prerequisites

Before running the application, make sure you have:

- Node.js installed.
- MongoDB database (local MongoDB or MongoDB Atlas).
- Git installed.
- A Gmail account with an App Password for email functionality.

## Installation and Setup

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd EventSphere
```

### 2. Configure Environment Variables

Navigate to the `server` folder and create a `.env` file.

Add the following configuration:

```env
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
EMAIL_USER=your_gmail_address
EMAIL_PASS=your_gmail_app_password
PORT=5000
```

Replace the placeholder values with your actual credentials.

**Note:** An App Password is required for Gmail SMTP authentication. Do not share or upload your `.env` file to GitHub.

### 3. Install Dependencies

From the project root, run:

```bash
npm install
npm run install:all
```

Alternatively, install dependencies separately.

**Backend:**

```bash
cd server
npm install --legacy-peer-deps
```

**Frontend:**

```bash
cd client
npm install
```

### 4. Run the Application

To start the frontend and backend together, run the following command from the project root:

```bash
npm run dev
```

Alternatively, start them separately.

**Backend:**

```bash
cd server
npm run dev
```

Backend server:

```text
http://localhost:5000
```

**Frontend:**

```bash
cd client
npm run dev
```

Frontend server (typically):

```text
http://localhost:5173
```

## Payment Handling

EventSphere supports free and paid event bookings. Payment is handled manually by the administrator, who updates the payment status after reviewing the booking. The application does not currently integrate a third-party payment gateway.

## Future Improvements

- Improve event search and filtering.
- Enhance the user dashboard.
- Improve form validation and error handling.
- Add additional booking management features.
- Improve the overall user interface and experience.

## Acknowledgement

This project is based on the open-source **Eventora MERN application**.

Original repository: https://github.com/ShivaMani02/Eventora-MERN

The original project and its contributors are acknowledged. EventSphere is the working name for the customised version, and additional modifications will be documented separately.

## License

Refer to the original repository's license before redistributing or publishing a modified version.
