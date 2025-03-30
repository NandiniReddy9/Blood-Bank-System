🩸 Blood Bank System

📌 Overview

The Blood Bank System is a software application designed to manage blood donation, storage, and distribution efficiently. It bridges the gap between donors, blood banks, and recipients by ensuring the availability of blood in emergencies.

🚀 Key Features

🏥 1. User Management

User Registration & Login (Donors, Hospitals, Admins)

JWT Authentication for secure access

Profile Management (update contact info, blood group, last donation date)

Role-based Access Control (RBAC) for different user types

🩸 2. Donor Management

 Search & Filter Donors based on blood group and location

 Track Last Donation Date and eligibility for next donation

 SMS & Email Reminders for upcoming donation schedules

 Donation History tracking for registered donors

🏥 3. Hospital & Blood Bank Features

Hospitals Can Request Blood from available donors

 Live Blood Stock Monitoring with alerts on low inventory

 Manage Blood Requests & Approvals with status updates

 Dashboard for Blood Banks to monitor blood collection and supply

📦 4. Blood Inventory Management

 Track Available Blood Units for each blood group

 Add, Update, or Remove Stock with expiry tracking

 Blood Expiry Alerts to ensure safe blood donation practices

 Allocate Blood to Hospitals based on request priority

📩 5. Notifications & Alerts

Emergency Blood Requests Alerts for donors

SMS & Email Notifications for donation reminders

Low Inventory Warnings for hospitals and blood banks

Admin Broadcast Messages for urgent updates

🔄 6. Blood Donation Scheduling

 Schedule Donation Appointments at nearby blood banks

 Find Nearest Blood Bank with Google Maps integration

 Track Eligibility for Next Donation based on past donation history

 Automated Reminders for upcoming donation dates

🖥 7. Admin Dashboard

 Analytics & Reports on blood donations, requests, and stock levels

 View Registered Users (Donors, Hospitals, Blood Banks)

 Manage User Roles & Permissions (Admin, Donor, Hospital)

 System Logs & Activity Tracking for security

📡 8. API & Third-Party Integrations

 RESTful API for integration with hospital systems

 Google Maps API for donor & blood bank location tracking

SMS & Email Gateway Integration for notifications

 Hospital Management System Integration for real-time blood stock updates
 
🔐 9. Security & Compliance

 JWT-Based Secure Authentication

 Data Encryption for donor and patient data

 GDPR & HIPAA Compliance for data privacy

 Audit Logs & Monitoring for security tracking

🌍 10. Scalability & Cloud Deployment

☁ Cloud-Based Hosting (AWS, Heroku, DigitalOcean)

 Docker Support for containerized deployment

 Load Balancing & Auto-Scaling for handling high traffic

 CI/CD Integration with GitHub Actions for automated deployment

📡 API Reference

## API Reference


```http
  POST /api/auth/register
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `name` | `string` | **Required**. Full name of the user |
| `email` | `string` | **Required**. Email for authentication |
| `password` | `string` | **Required**. Secure password|
| `role` | `string` | **Required**. User role (donor, hospital, admin) |


```http
  Login User
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `email` | `string` | **Required**. User's registered email |
| `password` | `string` | **Required**. User's password|


```http
  Donar Details
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `id` | `string` | **Required**. ID of the donor |



```http
  Update Donor Info
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `id` | `string` | **Required**. ID of the donor|
| `last_donation_date` | `string` | **Required**. Date of last donation|


```http
 📩 Notification APIs
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `recipient_id` | `string` | **Required**. ID of the recipient|
| `message` | `string` | **Required**. Notification content|







## 📌 Appendix

### A. Status Codes
The API returns standard HTTP status codes to indicate the success or failure of requests:

| Status Code | Meaning                  | Description |
|------------|--------------------------|-------------|
| `200 OK`   | Success                  | The request was successful. |
| `201 Created` | Resource Created       | A new resource was successfully created. |
| `400 Bad Request` | Invalid Input      | The request contains incorrect or missing parameters. |
| `401 Unauthorized` | Authentication Failed | The user is not authenticated. |
| `403 Forbidden` | Access Denied        | The user does not have permission for this action. |
| `404 Not Found` | Resource Not Found   | The requested resource was not found. |
| `500 Internal Server Error` | Server Issue | An error occurred on the server side. |

---

### B. Authentication & Security
- The API uses **JWT (JSON Web Token)** authentication.
- Every request to protected routes must include a `Bearer Token` in the `Authorization` header:
  ```http
  Authorization: Bearer <your_jwt_token>


Contact & Support
For API support, contact:

Email: support@bloodbankapi.com

Phone: +91 123456789

Documentation: API Docs




🔑 Authentication & Security

The API uses JWT (JSON Web Token) authentication.
Every request to protected routes must include a Bearer Token in the Authorization header:

Authorization: Bearer <your_jwt_token>

🚀 Deployment Guide

🔧 Prerequisites

Ensure you have the following installed:

🐍 Python 3.x (For Django backend)

🗄 PostgreSQL/MySQL (Database)

🟢 Node.js & npm (For frontend, if applicable)

⚙️ Environment Configuration

Create a .env file:

SECRET_KEY=your-secret-key
DEBUG=False
DATABASE_URL=postgres://username:password@localhost:5432/bloodbank
ALLOWED_HOSTS=yourdomain.com
JWT_SECRET=your-jwt-secret
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_HOST_USER=your-email@gmail.com
EMAIL_HOST_PASSWORD=your-email-password

▶️ Run Locally (For Testing)

python manage.py runserver

📞 Contact & Support

For API support, contact:
📧 Email: support@bloodbankapi.com📞   Phone: +91 123456789📖    Documentation: API Docs

✨ Authors

👩‍💻 @nandinireddy

