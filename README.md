<div align="center">
```
██╗    ██╗ █████╗ ██╗   ██╗███████╗ █████╗ ██████╗ ███████╗██████╗
██║    ██║██╔══██╗╚██╗ ██╔╝██╔════╝██╔══██╗██╔══██╗██╔════╝██╔══██╗
██║ █╗ ██║███████║ ╚████╔╝ █████╗  ███████║██████╔╝█████╗  ██████╔╝
██║███╗██║██╔══██║  ╚██╔╝  ██╔══╝  ██╔══██║██╔══██╗██╔══╝  ██╔══██╗
╚███╔███╔╝██║  ██║   ██║   ██║     ██║  ██║██║  ██║███████╗██║  ██║
 ╚══╝╚══╝ ╚═╝  ╚═╝   ╚═╝   ╚═╝     ╚═╝  ╚═╝╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝
```

### *The world's most immersive AI travel planner.*

<br/>

[![Live Demo](https://img.shields.io/badge/🌍_Live_Demo-Try_Wayfarer-gold?style=for-the-badge)](https://wayfarer.app)
[![Gemini API](https://img.shields.io/badge/Powered_by-Gemini_AI-blueviolet?style=for-the-badge&logo=google)](https://ai.google.dev/)
[![Three.js](https://img.shields.io/badge/Globe-Three.js-black?style=for-the-badge&logo=three.js)](https://threejs.org)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

<br/>

> **You open 14 tabs every time you plan a trip.**  
> *Wayfarer closes all of them.*

<br/>

![Wayfarer Globe Preview](https://raw.githubusercontent.com/yourusername/wayfarer/main/docs/assets/globe-preview.gif)

</div>

---

## ✦ What Is Wayfarer?

Wayfarer is an **immersive travel planning platform** that replaces your chaotic multi-tab travel research with a single, cinematic experience. It is built on an interactive 3D globe and powered entirely by Google Gemini's generative AI context limits.

It detects where you are. You click where you want to go. It handles everything else.

---

## ✦ The Experience

> *A picture is worth a thousand words. A globe that reacts to your cursor is worth a thousand pictures.*

### 🌍 The Living Globe

The moment you land on Wayfarer, a **photorealistic 3D Earth** greets you. Your current location pulses with a live ring. Every country lights up when you hover, with its name floating above it. 

Click any country. The globe **cinematic-zooms** into it. 

### ✈️ Flight Arcs

Select a destination and watch a **beautiful animated arc** draw itself across the globe from your origin to your destination — the exact route, curved along the Earth's actual surface.

### 🗓️ Day-by-Day Itinerary

Google's Gemini API generates a **complete, structured day-by-day plan** based on your specific atmosphere preferences and budget limits — formatted in a gorgeous animated timeline on the right panel.

---

## ✦ Tech Stack

```
┌─────────────────────────────────────────────────────────┐
│                     FRONTEND                            │
│  React · Three.js · react-globe.gl · Framer Motion      │
└────────────────────┬────────────────────────────────────┘
                     │
┌────────────────────▼────────────────────────────────────┐
│                   AI ENGINE                             │
│     Google Gemini API · Structured JSON Output          │
│     Prompt: dates + budget + vibe → full itinerary      │
└─────────────────────────────────────────────────────────┘
```

*(Note: Wayfarer is currently a lightweight frontend application that leverages AI directly to construct experiences. A full backend aggregation layer is planned for V2!)*

---

## ✦ Architecture Deep Dive

### 🧠 AI Itinerary Engine

Gemini doesn't just list tourist spots. It leverages advanced contextual reasoning to plan your trip logically.

```json
// Input Parameters
{
  "origin": "Your Location",
  "destination": "Target Country / City",
  "duration": 5,
  "budget": "moderate",
  "vibe": "adventurous"
}

// Output → Fully rendered in React Components
{
  "days": [
    {
      "day": 1,
      "title": "Arrival & Initial Exploration",
      "activities": [
        { "time": "Morning", "location": "City Center", "description": "..." }
      ],
      "accommodation": "Central Hotel"
    }
  ],
  "weatherForecast": "Temperatures around 72°F..."
}
```

---

## ✦ Getting Started

### Prerequisites

```bash
node >= 18.0.0
npm >= 9.0.0
```

### Installation

```bash
# 1. Clone the repo
git clone https://github.com/yourusername/wayfarer.git
cd wayfarer

# 2. Install dependencies
npm install

# 3. Set up environment variables
cp .env.local.example .env.local
```

### Environment Variables

To run the application, you only need one API key:

```env
# AI
GEMINI_API_KEY=your_gemini_api_key_here
```

### Run Locally

```bash
# Start frontend development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) and the globe is live.

---

## ✦ Project Structure

```
wayfarer/
├── src/
│   ├── components/
│   │   ├── Globe.jsx         ← Three.js globe + flight arcs
│   │   ├── LoadingScreen.jsx ← Cinematic entry sequence
│   │   └── ui/               ← Shadcn UI components
│   ├── services/
│   │   └── aiService.js      ← Gemini API integration
│   ├── lib/                  
│   │   └── utils.js          ← Styling utilities  
│   └── App.jsx               ← Main experience layout
│
├── .env.local                ← API keys
└── package.json
```

---

## ✦ Roadmap

- **v1.0** — Interactive 3D Globe + AI Itinerary Engine ← *we are here*
- **v1.5 (Planned)** — Hotel availability, live weather overlays via OpenWeather APIs
- **v2.0 (Planned)** — MongoDB backend for GeoJSON indexing & Redis caching for flight data
- **v3.0 (Planned)** — Collaborative trip rooms via WebSockets

---

## ✦ Contributing

Pull requests are genuinely welcome. This project is built in public.

```bash
# 1. Fork the repo
# 2. Create your feature branch
git checkout -b feature/new-globe-layers

# 3. Commit your changes
git commit -m "feat: add weather texture layer to globe"

# 4. Push and open a PR
git push origin feature/new-globe-layers
```

---

## ✦ License

MIT — use it, build on it, ship it.

---

<div align="center">

**Built with obsessive attention to detail.**

*If you've read this far — you should just try it.*

[![Try Wayfarer](https://img.shields.io/badge/🌍_Open_Wayfarer-Let's_Go-gold?style=for-the-badge)](https://wayfarer.app)

<br/>

Made with ❤️ and way too many late nights.

</div>
