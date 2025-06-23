# 📬 XKCD Email Comic Subscription System

This is a PHP-based web application that allows users to subscribe to receive a **random XKCD comic** every 24 hours via email. The system includes user **email verification**, **unsubscribe** functionality, and an automated **CRON job** to fetch and send comics daily.

---

## 🌟 Key Features

### ✅ Email Verification
- Users enter their email to subscribe.
- A **6-digit code** is sent to the email for verification.
- Upon successful verification, the email is stored for daily XKCD updates.

### ✅ XKCD Comic Delivery
- A CRON job runs every 24 hours to:
  - Fetch a random XKCD comic.
  - Format it as **HTML**.
  - Send the comic to all verified users.

### ✅ Unsubscribe Functionality
- Each email includes an **unsubscribe link**.
- Users can enter their email, receive a code, and confirm unsubscription.

---

## 🛠 Technologies Used

- PHP (v8.3)
- CRON Jobs (Linux)
- Mail Function (`mail()`)
- HTML for email formatting
- Bash scripting (`setup_cron.sh`)

---

## 🚀 How to Run Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/krupamohan/xkcd-email-subscription.git
   cd xkcd-email-subscription/src
2.	Start a local PHP server:
    php -S localhost:8000
3.	Open your browser and go to http://localhost:8000/index.php.
4.	To schedule the CRON job:
    bash setup_cron.sh

📩 Email Format Examples

✅ Verification Email
Subject: Your Verification Code
    <p>Your verification code is: <strong>123456</strong></p>

✅ Unsubscribe Confirmation Email
Subject: Confirm Un-subscription
    <p>To confirm un-subscription, use this code: <strong>654321</strong></p>
