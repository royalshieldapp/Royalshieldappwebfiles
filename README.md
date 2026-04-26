# Royal Shield Web App

React + Vite + Tailwind + Firebase starter for the Royal Shield private web app.

## What this project includes

- Login page
- Register page
- Protected dashboard
- Royal Shield sidebar layout
- Firebase Auth connection
- Firestore starter user profile
- Dashboard pages:
  - Malware Scan
  - VPN Status
  - SMS Phishing Guard
  - AI Hub
  - Privacy Center
  - Tracking Child
  - Subscription
  - Settings
- Firebase Hosting config

## Important architecture

Use this separation:

```txt
www.royalshield.app  -> public website, SEO, blog, academy, Ezoic
app.royalshield.app  -> private web app, login, dashboard, tools
```

Do not place Ezoic ads inside login, dashboard, settings, subscription, scanner, or private tools.

## Setup

```bash
npm install
cp .env.example .env
npm run dev
```

Then paste your Firebase values into `.env`.

## Firebase setup

Enable:

- Authentication -> Email/Password
- Firestore Database
- Hosting

## Build

```bash
npm run build
```

## Deploy to Firebase Hosting

```bash
npm install -g firebase-tools
firebase login
firebase init hosting
npm run firebase:deploy
```

When Firebase asks for public directory, use:

```txt
dist
```

When it asks if it is a single page app, choose:

```txt
Yes
```

## GitHub upload

```bash
git init
git add .
git commit -m "Initial Royal Shield web app"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/royal-shield-webapp.git
git push -u origin main
```
