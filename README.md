# TestPilot AI Portfolio — Setup Guide

## Files
- `index.html` — Main portfolio site
- `admin.html` — Admin panel to manage content

---

## Step 1: Firebase Setup (Free)

1. Go to https://console.firebase.google.com
2. Click "Add Project" → Name it "testpilot-portfolio"
3. Disable Google Analytics → Create Project

### Enable Firestore
- Left menu → Build → Firestore Database
- Click "Create Database"
- Select "Start in test mode" → Next → Done

### Enable Authentication
- Left menu → Build → Authentication
- Click "Get Started"
- Click "Email/Password" → Enable → Save
- Click "Add User" → Enter your email + password → Add

### Get Config
- Left menu → Project Settings (gear icon)
- Scroll to "Your apps" → Click </> (Web)
- Register app name: "portfolio"
- Copy the firebaseConfig object

---

## Step 2: Paste Config

Open BOTH `index.html` and `admin.html`

Find this section in BOTH files:
```javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  ...
```

Replace with your actual config from Firebase.

---

## Step 3: Deploy on Vercel (Free)

1. Go to https://vercel.com → Sign up free
2. Click "Add New Project"
3. Upload folder OR connect GitHub
4. Deploy — done!

Your site will be live at: `yourname.vercel.app`

---

## Step 4: Use Admin Panel

1. Go to `yoursite.vercel.app/admin.html`
2. Login with email/password you created in Firebase
3. Update content → Save
4. Changes appear on main site instantly!

---

## Admin Panel Features

| Section | What You Can Edit |
|---------|------------------|
| Hero | Headline, stats, availability tag |
| Services | All 6 service cards, pricing |
| Projects | Add/delete case studies |
| Skills | Skill percentages, tool badges |
| Contact | Email, Upwork, LinkedIn links |

---

## Adding First Project (Sample Audit)

1. Open admin.html → Projects tab
2. Fill: Name = "E-commerce App Audit (Sample)"
3. Type = QA Audit, Status = Sample
4. Add metrics: "12 | Bugs Found", "94 | Performance Score"
5. Add tags: Manual Testing, Mobile, Chrome DevTools
6. Click Add Project

This shows on your portfolio instantly!
