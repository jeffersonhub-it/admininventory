# Deploy to Firebase Hosting

Run these inside this folder:

    npm install -g firebase-tools
    firebase login
    firebase deploy --only firestore:rules,hosting

Your app will be live at:
    https://admininventory-c11ae.web.app
    https://admininventory-c11ae.firebaseapp.com

Before first use, finish the console setup:
1. Authentication > Sign-in method > enable Email/Password
2. Firestore Database > Create database (if not yet created)
3. Create the default accounts (one command, see scripts/seed-accounts.js):

       iss   / smeagol  -> HEAD ADMIN    (full access)
       admin / admin1   -> ADMINISTRATOR (adds/encodes RS; in RRS can only edit Status + Remarks)

   Download a service account key (Project settings > Service accounts) to
   scripts/serviceAccountKey.json, then:

       cd scripts && npm install firebase-admin && node seed-accounts.js

   (Do not commit serviceAccountKey.json. Change the passwords in Settings after first login.)

Hosting domains (web.app / firebaseapp.com) are authorized for Auth automatically.
