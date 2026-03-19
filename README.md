#VARANASI — Official Countdown Page

A cinematic, browser-based movie countdown page for **Varanasi (2027)** — starring Mahesh Babu, Priyanka Chopra, and Prithviraj, directed by SS Rajamouli. Features a live countdown timer, rotating background posters, ambient music toggle, and social sharing.

---

## ✨ Features

- **Live countdown timer** — years, months, days, hours, minutes, seconds to April 7, 2027 (IST)
- **Rotating cinematic backgrounds** — auto-transitions between movie posters every 8 seconds with smooth fade
- **Ambient music toggle** — background score with mute/unmute button; respects browser autoplay policy
- **Stone-carved title effect** — layered CSS text-shadow and pseudo-elements create an engraved stone look
- **Devanagari overlay** — subtle `वाराणसी` watermark behind the Latin title
- **Trailer button** — opens the official YouTube trailer in a new tab
- **Share button** — uses the native Web Share API for mobile sharing
- **Fully responsive** — adapts to mobile and desktop viewports

---

## 📁 Project Structure
```
varanasi-countdown/
├── index.html                  # Main countdown page (single file)
├── Varanasi_ The Arrival.mp3   # Background ambient audio
└── README.md
```

> Background poster images are loaded from external URLs. No local image assets required.

---

## 🚀 Getting Started

### 1. Clone or download
```bash
git clone https://github.com/your-username/varanasi-countdown.git
cd varanasi-countdown
```

### 2. Add the audio file

Place `Varanasi_ The Arrival.mp3` in the same directory as `index.html`.

### 3. Open in a browser
```bash
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

No build tools, no dependencies, no server required.

---

## ⚙️ Configuration

All key values live inside `index.html`:

### Release date
```js
const releaseDate = new Date("2027-04-07T00:00:00+05:30");
```

### Background posters
```js
const posters = [
  "https://your-image-url-1.jpg",
  "https://your-image-url-2.jpg",
  "https://your-image-url-3.jpg"
];
```

### Trailer link
```js
function openTrailer() {
  window.open("https://youtu.be/YOUR_VIDEO_ID", "_blank");
}
```

### Audio file
Replace `Varanasi_ The Arrival.mp3` with any `.mp3` and update the `<source src="...">` tag.

---

## 🌐 Deployment

Static HTML — deploy anywhere:

| Platform | How |
|---|---|
| **GitHub Pages** | Push repo → enable Pages from `main` branch |
| **Netlify** | Drag and drop the folder at netlify.com |
| **Vercel** | Run `vercel --prod` from the project directory |
| **Any web host** | Upload `index.html` + `.mp3` via FTP/cPanel |

---

## 🛠️ Built With

- Vanilla HTML, CSS, JavaScript — zero dependencies
- [Google Fonts](https://fonts.google.com/) — Cinzel, Cinzel Decorative, Noto Serif Devanagari
- Web Share API for native mobile sharing
- HTML `<audio>` element for background music

---

## 📱 Browser Compatibility

| Browser | Support |
|---|---|
| Chrome / Edge | ✅ Full |
| Firefox | ✅ Full |
| Safari (iOS) | ✅ Full (share requires HTTPS) |
| Opera | ✅ Full |

> `navigator.share` (Share button) only works on HTTPS and supported mobile browsers. It silently does nothing elsewhere.

---

## 📄 License

Fan/promotional project. All movie assets, names, and likenesses belong to their respective rights holders.
