# 🚗 Parkify – Smart Parking Reservation & Management System

A Flask-based smart parking platform that allows users to discover parking facilities, reserve parking capacity in advance, and receive QR-based verification for dynamic slot allocation. Parkify also includes machine-learning-based parking demand prediction and alternative parking recommendations.

## 📌 Project Overview

Finding available parking can be inconvenient, especially near busy locations such as malls, hospitals, and theatres.

Parkify aims to simplify this process by providing a centralised platform where customers can explore parking facilities, book in advance, and complete a demo payment. Instead of reserving a specific physical slot, the system reserves parking capacity and assigns an available slot dynamically when the customer arrives and presents their QR code.

## ✨ Key Features

### 👤 User Management
- Customer, parking owner, and administrator roles.
- User registration and login.
- Role-based dashboards and access.

### 🅿️ Parking Discovery & Booking
- View available parking facilities and their details.
- Check parking capacity and hourly pricing.
- Select booking date, start time, and duration.
- Reserve parking capacity in advance.
- Automatic booking confirmation.

### 📱 QR-Based Verification & Dynamic Slot Allocation
- Generate a unique QR code for confirmed bookings.
- Verify bookings through QR scanning or booking ID.
- Assign an available physical parking slot dynamically upon arrival.
- Support check-in and check-out operations.

### ⏳ Waiting List Management
- Allow customers to join a waiting list when a facility is full.
- Offer newly available capacity to the next customer in the queue.
- Provide a 15-minute acceptance window.
- Expire unanswered offers and move to the next customer.

### 💳 Payment & Cancellation
- Demo-mode payment recording.
- Cancellation with a 70% refund calculation.
- No-show handling without a refund.
- Booking and payment status tracking.

### 🤖 Machine Learning – Parking Demand Prediction
- Predict parking demand as Low, Medium, or High.
- Consider features such as arrival hour, occupancy, weekday, and price.
- Display estimated available spaces and model confidence.
- Recommend alternative parking facilities based on predicted demand, current availability, and hourly price.

**Note:** The ML model is a demonstration prototype trained on generated synthetic sample data. Its predictions are illustrative and have not been validated against real-world parking data.

### 📊 Dashboards
- **Customer Dashboard:** Parking discovery, demand forecasts, recommendations, bookings, and notifications.
- **Owner Dashboard:** Parking facility management and booking operations, including QR verification.
- **Admin Dashboard:** Overview of users, parking facilities, bookings, and recorded revenue.

## 🛠️ Technologies Used

| Category | Technologies |
|---|---|
| Backend | Python, Flask |
| Frontend | HTML, CSS |
| Database | SQLite |
| Machine Learning | Scikit-learn |
| QR Code Generation | Python QR code library |
| Version Control | Git, GitHub |

## ⚙️ Installation & Setup

### Prerequisites
- Python 3.10 or later
- Git

### 1. Clone the repository

```bash
git clone https://github.com/Dev-Darsh/Parkify.git
cd Parkify
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows:

```powershell
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the application

```bash
python app.py
```

### 5. Open Parkify

Visit:

```text
http://127.0.0.1:5000
```

## 🧠 Machine Learning Approach

Parkify uses a Random Forest classification model to demonstrate parking demand prediction.

The model uses generated sample data containing features such as:
- Arrival hour
- Weekday
- Parking occupancy
- Parking price
- Weekend indicator

The model classifies expected demand into three categories:

- **Low Demand**
- **Medium Demand**
- **High Demand**

The predicted demand is displayed on the customer dashboard and contributes to alternative parking recommendations.

Since the training data is synthetic, the model demonstrates the ML workflow rather than providing production-grade forecasts.

## 📁 Project Structure

```text
Parkify/
│
├── app.py
├── parking_ml.py
├── requirements.txt
├── README.md
├── .gitignore
│
├── static/
│   └── style.css
│
└── templates/
    ├── admin_dashboard.html
    ├── base.html
    ├── booking.html
    ├── booking_success.html
    ├── dashboard.html
    ├── index.html
    ├── login.html
    ├── message.html
    ├── my_bookings.html
    ├── notifications.html
    └── owner_dashboard.html
```

## 🎯 Project Objective

The objective of Parkify is to demonstrate how web development, database management, QR-based verification, dynamic resource allocation, and machine learning can be integrated into a smart parking management platform.

## 👥 Project Team

- B S Dev Darsh
- Jensen Jose Sajan
- Krishna SP
- Rishika Kunnumpurath Chali

## ⚠️ Disclaimer

Parkify is an academic software engineering prototype. Payments are recorded in demo mode and do not involve a real payment gateway. ML predictions use synthetic training data and should not be treated as validated real-world forecasts.

## 🔗 Repository

[GitHub – Dev-Darsh/Parkify](https://github.com/Dev-Darsh/Parkify)

---

⭐ If you find this project interesting, consider giving the repository a star!
