# ✨ Special Birthday Wish Web App ✨

A premium, interactive, and beautifully designed birthday celebration web application built using HTML, CSS, JavaScript, and GSAP. This application is designed to create a magical and memorable experience for the birthday person.

---

## 🌟 Live Demo & Flow

The web application consists of a choreographed multi-page celebration flow:

### 1. The Entrance ([index.html](file:///d:/New%20folder/Birthday%20wish%20web/birthday-main/index.html))
*   **Visuals:** Elegant glassmorphic container set against a slowly changing gradient background, accented by ambient floating bubbles, star dust particles (`dustCanvas`), and floating emojis.
*   **Interactivity:** Prompts the user to enter their name (defaults to "Sree"). On click, it triggers a custom heart physics trail, shows a celebration GIF, and launches the persistent background music.
*   **Data Persistence:** Saves the name in `localStorage` to personalize the rest of the experience.

### 2. The Celebration ([birthday.html](file:///d:/New%20folder/Birthday%20wish%20web/birthday-main/birthday.html))
*   **Visuals:** A dark starry night sky with three concurrent canvas animation layers:
    1.  *Twinkling Stars Sky* (`starCanvas`)
    2.  *Falling Rose Petals* (`petalsCanvas`)
    3.  *Fireworks Splash* (`fireworksCanvas`)
*   **Interactivity:** Displays a personalized birthday title ("Happy Birthday, Sree") with letters animated via GSAP stagger waves. Users can click anywhere on the background to manually launch customized heart-shaped fireworks.
*   **Navigation:** A smooth slide-in button directs the user to the cake-cutting ceremony.

### 3. The Candle Blowing ([cake.html](file:///d:/New%20folder/Birthday%20wish%20web/birthday-main/cake.html))
*   **Visuals:** A layered 3D cake with realistic frosting, cream drips, and colorful sprinkles. A glowing, flickering candle sits on top.
*   **Interactivity:** Uses the **Web Audio API** to detect microphone input! The user can blow into their microphone to extinguish the candle flame, or click the cake as a fallback.
*   **Celebration:** Blowing out the candle triggers a massive confetti particle explosion and unlocks the "Open Card" action button.

### 4. Memory Lane & Wishes Dashboard ([final.html](file:///d:/New%20folder/Birthday%20wish%20web/birthday-main/final.html) & [style.css](file:///d:/New%20folder/Birthday%20wish%20web/birthday-main/style.css))
*   **Visuals:** A split dashboard design with a dark cosmic backdrop and glowing background orbs.
*   **3D Flipping Card:** A realistic card that flips 180° on click, revealing a polaroid photo frame and a sweet signature.
*   **Memory Lane:** A polaroid picture deck showing shared moments, equipped with an interactive 3D mouse/touch tilting effect.
*   **Balloon Popping Game:** Floating helium balloons that wobble and float. Clicking a balloon pops it with a GSAP scaling animation, revealing personalized pop-up cards containing heartfelt wishes.

---

## ⚙️ Core Technical Features

### 🎵 Persistent Background Music Engine ([music.js](file:///d:/New%20folder/Birthday%20wish%20web/birthday-main/music.js))
*   Manages the playback of the background music theme `Happy Birthday My Love  - Friz Love(MP3_160K).mp3`.
*   **Continuous Playback:** Uses `localStorage` to save and resume the audio playback position (`currentTime`) and playback state (`playing`) across all pages.
*   **Smooth Transitions:** Implements volume fade-in on load and fade-out on pause or redirect.
*   **Glassmorphic Floating Player:** Places a gorgeous floating controller in the bottom-left corner of all pages. Features a bouncing music note emitter and an active audio visualizer bar indicator.

### 🎨 Premium Styling & Micro-Animations
*   **Glassmorphism:** Uses `backdrop-filter: blur()`, semi-transparent borders, and inner box-shadow highlights for a modern UI.
*   **Smooth Animations:** Powered by **GSAP** (GreenSock Animation Platform) for letter staggers, physics-based heart bursts, and springy button scaling.
*   **Responsiveness:** Tailored using fluid CSS variables, Flexbox/Grid layouts, and media queries to look great on desktop, tablet, and mobile screens.

---

## 📂 Project Structure

```
Birthday wish web/
│
├── birthday-main/
│   ├── index.html                                 # Intro / Name input page
│   ├── birthday.html                              # Wishes, starry sky & fireworks page
│   ├── cake.html                                  # 3D Cake cutting & mic blow page
│   ├── final.html                                 # Dashboard (Flipping card, Polaroids & Balloon game)
│   ├── music.js                                   # Shared persistent BGM controller script
│   ├── style.css                                  # Custom dashboard styles
│   ├── Happy Birthday My Love - Friz Love.mp3     # Celebration background audio
│   │
│   └── images/
│       ├── penguin.jpg                            # Card photo
│       ├── gif_1.gif                              # Intro GIF decoration
│       └── [other assets/gifs]
│
└── README.md                                      # Project documentation
```

---

## 🚀 How to Run Locally

Since the application uses the **Web Audio API** (microphone detection) and **LocalStorage** for name and BGM tracking:

1.  **Standard Launch:** Double-click [index.html](file:///d:/New%20folder/Birthday%20wish%20web/birthday-main/index.html) to open it in any modern web browser.
2.  **Recommended (Local Server):** To ensure full browser permission support for audio and microphone features, run a local development server:
    *   **NodeJS:** Run `npx live-server` inside the `birthday-main/` folder.
    *   **Python:** Run `python -m http.server` in the `birthday-main/` folder.
    *   **VS Code:** Use the *Live Server* extension.

---
*Created with 💖 to make a special day even more magical.*
