# FC 26 Career Tracker 2.0 - Setup

## Firebase instellen (gratis, 5 minuten)

### 1. Firebase project aanmaken
1. Ga naar https://console.firebase.google.com
2. Klik **Project toevoegen**
3. Noem het bijv. `fc26-tracker`
4. Google Analytics mag je uitzetten, niet nodig
5. Klik **Project aanmaken**

### 2. Firestore database aanmaken
1. In je Firebase project, klik links op **Firestore Database**
2. Klik **Database aanmaken**
3. Kies **Start in test mode** (makkelijkst)
4. Kies een locatie (europe-west1 is prima)
5. Klik **Inschakelen**

### 3. Authentication aanzetten
1. Klik links op **Authentication**
2. Klik **Aan de slag**
3. Ga naar tabblad **Sign-in method**
4. Klik op **Anoniem** en zet het **aan**
5. Klik **Opslaan**

### 4. Web-app toevoegen
1. Ga naar **Projectinstellingen** (tandwiel icoon linksboven)
2. Scroll naar beneden en klik het **</>** icoon (Web)
3. Noem het bijv. `fc26-web`
4. Vink **Firebase Hosting** NIET aan
5. Klik **App registreren**
6. Je krijgt nu een config blok te zien met `apiKey`, `authDomain`, etc.

### 5. Config invullen
Open `index.html` en zoek bovenaan naar `FIREBASE CONFIG HIER` - vervang de lege waardes met jouw config:

```js
const firebaseConfig = {
  apiKey: "jouw-api-key",
  authDomain: "jouw-project.firebaseapp.com",
  projectId: "jouw-project-id",
  storageBucket: "jouw-project.appspot.com",
  messagingSenderId: "123456789",
  appId: "jouw-app-id"
};
```

### 6. Online zetten
Upload de bestanden naar GitHub Pages (zie de uitleg in de oude versie) of Netlify.

Dat is alles! Jij en je vriend(en) openen dezelfde URL, kiezen een naam, en kunnen elkaars career modes zien.
