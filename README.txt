LUMORA BOOKS — WEBSITE + 3 BOOK APIs

WHAT IS INCLUDED
- Responsive book discovery website
- Search, category/year filters, sorting and pagination
- Book details and favourites
- Open Library Search API
- Google Books API
- Gutendex API (Project Gutenberg catalogue)
- Optional Firebase cloud sync for saved favourites

IMPORTANT: HOW TO LET OTHER PEOPLE VIEW YOUR WEBSITE
Running Live Server only makes the website available on your own computer.
To let other people visit it, publish this folder using a static website host.

EASIEST METHOD — NETLIFY DROP
1. Extract this ZIP file.
2. Open https://app.netlify.com/drop in your browser.
3. Sign in or create a Netlify account if asked.
4. Drag the extracted lumora-books folder (the folder containing index.html)
   onto the Netlify Drop page.
5. Wait for publishing to finish. Netlify will give you a public website URL.
6. Copy that URL and send it to other people. They can open it on their phones
   or computers, as long as they have internet access.

ALTERNATIVE — GITHUB PAGES
1. Create a GitHub repository and upload all files from this folder.
2. Open the repository Settings > Pages.
3. Under Build and deployment, choose Deploy from a branch.
4. Choose the main branch and /(root), then Save.
5. Wait for GitHub Pages to publish and use the URL it provides.

RUN LOCALLY FOR TESTING
- Open this folder in Visual Studio Code.
- Right-click index.html and choose Open with Live Server.
- Do not double-click index.html; ES modules work best through a local web server.

ABOUT THE APIs
1. Open Library: https://openlibrary.org/search.json?q=harry+potter
2. Google Books: https://www.googleapis.com/books/v1/volumes?q=harry+potter
3. Gutendex: https://gutendex.com/books/?search=pride
The basic search endpoints used here do not require an API key. Internet access
is required. An API provider may occasionally be slow, rate-limit requests, or
be temporarily unavailable. If one source fails, choose another in the API menu.

ABOUT FAVOURITES
Without Firebase setup, favourites are saved only in the current browser/device.
They do NOT automatically appear on another person's device.
To sync a user's own favourites across their devices, configure Firebase below.
Each visitor gets their own private library; this project does not create one
shared public favourites list.

OPTIONAL FIREBASE CLOUD SYNC
1. Create a Firebase project and register a Web App.
2. Copy the Firebase web configuration into firebase.js, replacing placeholders.
3. Enable Authentication > Sign-in method > Anonymous.
4. Create a Cloud Firestore database.
5. Publish the rules in firestore.rules in Firebase Console > Firestore > Rules.
6. Add your deployed website domain under Firebase Authentication > Settings >
   Authorized domains if Firebase requires it.
Do not put service-account credentials or private server keys in this website.
The Firebase web config is intended for client apps; protect data with Firestore
Security Rules.

TROUBLESHOOTING
- Blank page: check the browser Console (F12) for a red error.
- Books do not load: check internet access and try a different API source.
- Other people cannot open it: publish it using Netlify Drop or GitHub Pages,
  then share the public URL (not localhost or a Live Server address).
- Favourites do not transfer to another device: configure Firebase cloud sync.
