# OPSCOM — Tactical Comms Terminal

A real-time military ops-style chat for you and your friends, hosted on GitHub Pages.

## Setup (5 minutes)

### Step 1 — Firebase (free backend)
1. Go to [console.firebase.google.com](https://console.firebase.google.com)
2. Click **Add project** → name it anything → click through
3. On the project homepage, click **</>** (Web) to add a web app
4. Name it anything → click **Register app**
5. Copy the `firebaseConfig` object that appears

### Step 2 — Realtime Database
1. In the left sidebar, go to **Build → Realtime Database**
2. Click **Create Database** → pick a region → start in **test mode**
3. That's it — the database is ready

### Step 3 — Paste config into index.html
Open `index.html` and find this section near the bottom:

```js
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  ...
};
```

Replace the whole object with your actual config from Step 1.

### Step 4 — GitHub Pages
1. Create a new GitHub repo (public)
2. Upload `index.html`
3. Go to **Settings → Pages → Source: main branch / root**
4. Your site will be live at `https://yourusername.github.io/your-repo`

Share that URL with your friends. Anyone who visits it can pick a callsign and start transmitting in real time.

## Features
- Real-time messaging via Firebase Realtime Database
- Callsign identity system
- Online agents list in sidebar
- Military ops / CRT terminal aesthetic
- Works on mobile too

## Security Note
This uses Firebase in "test mode" (open read/write). Fine for friends — if you want to lock it down, add Firebase Authentication or IP rules in the Firebase console.
