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
3. Create the first admin (Auth user iss@admininventory.local + Firestore users/{UID} doc
   with role=admin, status=APPROVED, department=ISS, username=iss, fullName=ISS Admin)

Hosting domains (web.app / firebaseapp.com) are authorized for Auth automatically.
