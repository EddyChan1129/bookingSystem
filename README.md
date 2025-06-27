# 🗓️ Booking System (Calendly Clone)

This is a simple full-stack booking system where tutors can create available time slots and students can book appointments. It supports Google Calendar integration and email notifications.

## 🔧 Tech Stack

- **Next.js** – React framework for full-stack web development
- **TypeScript** – Type-safe JavaScript
- **Clerk** – Authentication (Sign in / Sign up)
- **PostgreSQL** – Relational database
- **Google Calendar API** – Sync bookings with Google Calendar
- **Tailwind CSS** – Styling

## 📁 Environment Variables

Create a `.env.local` file and add the following variables:

```env
DATABASE_URL=your_postgresql_url

GOOGLE_OAUTH_CLIENT_ID=your_google_client_id
GOOGLE_OAUTH_CLIENT_SECRET=your_google_client_secret
GOOGLE_OAUTH_REDIRECT_URL=http://localhost:3000/api/auth/callback/google

NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up

NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
CLERK_SECRET_KEY=your_clerk_secret_key
````

## 🔑 How to Get Your API Keys

### 1. **Google OAuth**

* Go to [Google Cloud Console](https://console.cloud.google.com/)
* Create a new project
* Enable `Google Calendar API`
* Set up OAuth 2.0 credentials
* Add authorized redirect URI:

  ```
  http://localhost:3000/api/auth/callback/google
  ```

### 2. **Clerk**

* Go to [Clerk Dashboard](https://clerk.dev/)
* Create a new application
* Copy the following from your dashboard:

  * **Publishable Key**
  * **Secret Key**
  * Set redirect URLs to:

    * `http://localhost:3000/sign-in`
    * `http://localhost:3000/sign-up`

## 🧪 Local Development

```bash
# Install dependencies
npm install

# Run development server
npm run dev

# App will be running at:
http://localhost:3000
```

## 📌 Features

* Tutor sign up and login (via Clerk)
* Student booking interface
* Google Calendar integration
* Email notifications (optional: can integrate nodemailer)
* PostgreSQL backend using Prisma (if applicable)

