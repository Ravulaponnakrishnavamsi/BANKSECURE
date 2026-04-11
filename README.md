# SecureBank – High Performance OTP App (Clean Refactor)

A professional, high-speed banking web app focused on instant OTP verification using Node.js/Express and In-Memory storage. 

> [!IMPORTANT]
> **Firebase Removal complete**: This project no longer uses Firebase or MongoDB. It is designed for maximum speed and simplicity using server memory.

## 🚀 Setup & Installation

### 1. Prerequisites
- Node.js (v18+)
- Gmail Account (for sending OTPs)

### 2. Environment Variables (.env)
Create a `.env` file in the root directory:
```env
PORT=5000
RESEND_API_KEY=re_123456789
OWNER_EMAIL=your-recipient-email@gmail.com
JWT_SECRET=super-secret-key-change-me
```

### 3. Install & Start
```bash
npm install
npm run dev
```

## 🌍 Deployment on Render (Step-by-Step)

If the OTP system is not working on your live URL, follow these exact steps to fix it:

1.  **Login to Render**: Go to your [Render Dashboard](https://dashboard.render.com).
2.  **Select your Web Service**: Click on `securebank-app`.
3.  **Go to Environment Settings**: Click **"Environment"** in the left sidebar.
4.  **Update Variables**: Ensure the following keys are **exactly** correct:
    -   `RESEND_API_KEY`: Your API key from Resend.com.
    -   `OWNER_EMAIL`: The email where you want to receive OTPs.
    -   `JWT_SECRET`: Any random string.
    -   *Delete `GMAIL_USER`, `GMAIL_APP_PASSWORD`, and `FIREBASE_SERVICE_ACCOUNT`* as they are no longer used.
5.  **Save Changes**: Click "Save Changes". Render will automatically restart your app.

## 📁 Project Structure (Senior Architect Level)
- `/src/controllers` - Auth logic (Send/Verify OTPs).
- `/src/routes` - API Route definitions.
- `/src/utils` - Mailer and Memory Store helpers.
- `server.js` - Optimized entry point.

## 📜 How to Commit Changes
1. `git add .`
2. `git commit -m "feat: senior refactor - firebase removed - high speed memory auth"`
3. `git push origin main`
