# RiskaNova -- Secure Access Control Management System

## Problem Statement

Traditional authentication systems rely only on username and password
verification, making them vulnerable to unauthorized access, brute-force
attacks, and suspicious login attempts.

There is a need for a Secure Access Control Management System that
dynamically evaluates the risk associated with each login attempt and
applies adaptive security mechanisms accordingly.

This project implements a Risk-Based Authentication System that
classifies login attempts into:

-   Low Risk
-   Medium Risk
-   High Risk

Based on the calculated risk level, the system enforces appropriate
security measures such as OTP verification or access blocking.

------------------------------------------------------------------------

## Objectives

-   Implement a secure login system using Flask.
-   Introduce risk-based authentication logic.
-   Apply Multi-Factor Authentication (OTP) for medium-risk logins.
-   Automatically block high-risk login attempts.
-   Ensure secure session management.

------------------------------------------------------------------------

## Key Features

-   User Authentication (Username & Password)
-   Risk-Based Access Control
-   Time-Based Risk Detection
-   Random Anomaly Simulation
-   OTP Verification for Medium Risk
-   Session-Based Dashboard Protection
-   Logout and Session Clearing Mechanism

------------------------------------------------------------------------

## How It Works

### 1. Login Authentication

Users enter their username and password.\
The system validates credentials against stored user data.

### 2. Risk Calculation

Risk is calculated using: - Current login time\
- Random anomaly detection simulation

### 3. Risk-Based Decision

  Risk Level   Action
  ------------ ---------------------------
  Low          Direct Dashboard Access
  Medium       OTP Verification Required
  High         Access Blocked

### 4. OTP Verification

-   A 6-digit OTP is generated.
-   User must enter the correct OTP.
-   Access is granted upon successful verification.

### 5. Session Protection

Only authenticated users can access protected routes like the
dashboard.\
Logout clears session data securely.

------------------------------------------------------------------------

## Tech Stack

-   Backend: Python (Flask Framework)
-   Frontend: HTML, CSS
-   Session Management: Flask Sessions
-   Risk Logic: Python datetime and random modules

------------------------------------------------------------------------

## Installation & Setup

1.  Clone the repository\
    git clone https://github.com/your-username/RiskaNova.git\
    cd RiskaNova

2.  Install dependencies\
    pip install flask

3.  Run the application\
    python app.py

4.  Open in browser\
    http://127.0.0.1:5000/

------------------------------------------------------------------------

## Default Credentials

Username: admin\
Password: admin123

------------------------------------------------------------------------

## Future Enhancements

-   Implement password hashing
-   Store users in a database
-   Send OTP via Email or SMS
-   Add login attempt limits
-   Implement Role-Based Access Control

------------------------------------------------------------------------

## Conclusion

RiskaNova demonstrates how adaptive authentication enhances system
security compared to traditional static login systems.

By introducing dynamic risk evaluation and multi-factor verification,
the system provides stronger protection against unauthorized access
while maintaining usability for legitimate users.
