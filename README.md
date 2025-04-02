# Outfitly: Your Personal AI Fashion Stylist & Smart Wardrobe Agent

## 🧠 Overview

ClosetMind is a Progressive Web App (PWA) powered by AI, designed to act as your personal stylist, wardrobe organizer, and smart shopping advisor. It helps users manage their wardrobe, get daily outfit suggestions based on real-time context (weather, occasion, mood), and avoid impulsive purchases by recommending only meaningful additions to their collection.

> **Tagline:** "Think Before You Dress. Think Before You Buy."

> **Note:** This app is designed **exclusively for mobile-first experience**. Desktop versions are not supported to ensure a seamless and intuitive fashion assistant tailored for everyday smartphone use.

> **AI tool Instruction:** All components, layouts, styles, and logic generated or suggested using Gemini, Copilot, Cursor AI, or other AI tools should be optimized strictly for **mobile screen sizes only**. Avoid any desktop responsiveness, scaling, or features not intended for handheld use.

---

## ✨ Key Features

### 1. **Onboarding & Style Profiling**

- Style questionnaire to understand user preferences
- Collect climate data (via API or location input)
- Optional: Connect calendar for event-based dressing

### 2. **Wardrobe Management**

- Upload clothing items via camera or gallery
- Auto-tag clothes (type, color, season, formality) using image classification APIs
- Edit metadata (e.g., purchase date, brand, cost)
- Tracks wear history, last worn, usage count

### 3. **Daily Outfit Suggestions**

- Suggests outfits based on:
  - Weather (API)
  - Occasion (user-input or calendar)
  - Mood (optional input)
  - Recent outfits (avoid repeats)
- Mix & match from existing wardrobe
- Swipe interface: Accept / Shuffle / Save

### 4. **Shopping Recommendations**

- Detects wardrobe gaps (“You have 6 shirts but no jackets”)
- Based on usage data, suggests what you *actually need*
- Integrates with affiliate APIs (Amazon, Flipkart) for discovery

### 5. **Buy or Bail**

- User uploads screenshot or link of an item they’re planning to buy
- Agent analyzes:
  - Similarity to items in wardrobe
  - Potential outfit matches
  - Cost-per-wear estimation
  - Sentiment (impulse vs. planned)
- Final output: "Buy ✅" or "Bail ❌" with reasoning and alternatives

### 6. **PWA**

- Home screen installable (Android & iOS)
- Offline access to saved wardrobe and style history

---

## 🔧 Tech Stack

### 🖥 Frontend (PWA)

- **Framework**: React / Next.js
- **Styling**: Tailwind CSS
- **PWA Support**: `next-pwa`
- **State Management**: Redux (or React Context API)

### 🔍 AI & ML

- **LLM Agent**: Gemini 2.5 via LangChain
- **Image Labeling**: Replicate CLIP / Google Vision API
- **Agent Memory**: Vector DB (ChromaDB / Pinecone)

### 🧰 Backend & Storage

- **Auth + DB + Storage**: Supabase (auth, image storage, metadata)
- **Weather API**: OpenWeatherMap
- **Optional APIs**: Google Calendar API, Shopping APIs (Flipkart, Amazon)

---

## 🧱 Folder Structure Suggestion

```
/outfitly
├── public
│   └── manifest.json (PWA config)
├── src
│   ├── components
│   ├── pages
│   ├── styles
│   ├── store (Redux or context)
│   ├── lib (AI functions, API utils)
│   └── features
│       ├── wardrobe
│       ├── stylist
│       ├── shop-check
│       └── onboarding
└── supabase
    └── schema.sql
```

---

## 🚀 MVP Plan (Suggested Phases)

### 🔹 Phase 1 – Core Wardrobe + Outfit Agent

- Onboarding
- Upload wardrobe (photo + tagging)
- Daily outfit generation (based on weather)

### 🔹 Phase 2 – Buy or Bail + Recommendations

- Upload product screenshot/link
- Analyze + suggest
- Build missing items recommendation logic

### 🔹 Phase 3 – Polish & PWA Experience

- Offline storage
- Home screen install + polishing UI

---

## 💡 Future Enhancements

- Outfit visualization using AI (try-on view)
- Social lookbook sharing
- AI-generated style evolution timeline
- Local language support for wider Indian audience

---

## 📣 Contributors

- Solo Dev: Aryan Sahu
- Inspired by: Real-life frustration, minimalism, and Naruto’s Yamanaka Clan 🌀

---

## 🏁 License

MIT – Feel free to build, fork, and style the world ✨
