# 🌊 AquaAI — Intelligent Hydration & AI Coach

<p align="center">
  <b>A smart, native mobile app that turns everyday water tracking into a personalized, AI-powered health experience.</b>
</p>

<p align="center">
  <img alt="Platform" src="https://img.shields.io/badge/platform-Android%20%7C%20iOS-blue">
  <img alt="Built with Expo" src="https://img.shields.io/badge/built%20with-Expo%20SDK%2051-000020?logo=expo">
  <img alt="React Native" src="https://img.shields.io/badge/React%20Native-0.74-61DAFB?logo=react">
  <img alt="Firebase" src="https://img.shields.io/badge/backend-Firebase-FFCA28?logo=firebase">
  <img alt="License" src="https://img.shields.io/badge/license-MIT-green">
</p>

---

## 📖 Overview

**AquaAI** is a cross-platform mobile application built with **React Native** and **Expo (SDK 51)**. It helps users build healthier hydration habits by tracking daily water intake, calculating personalized hydration goals, and offering an interactive **AI Coach** that delivers lifestyle and sports-performance advice tailored to the user's activity and hydration score.

The app combines a clean, dark-first interface with real-time data sync — designed to feel fast, minimal, and genuinely useful for daily tracking.

---

## 🚀 Key Features

| Feature | Description |
|---|---|
| 💧 **Smart Hydration Tracking** | Log daily water intake through a clean, intuitive UI with real-time visual progress. |
| 🤖 **AI Coach Integration** | Chat with an AI mentor that gives hydration and performance insights based on your personal score. |
| 📊 **Personalized Analytics** | Dynamic daily goals and fluid logs powered by dedicated state stores (`goalStore`, `waterStore`). |
| ☁️ **Real-Time Sync** | Firebase Authentication and Firestore keep your data synced securely across sessions. |
| 🌙 **Dark-First UI** | A polished, immersive dark-mode interface designed for comfortable everyday use. |
| 📱 **Cross-Platform** | Built natively for both Android and iOS from a single codebase. |

---

## 🛠️ Tech Stack & Architecture

- **Frontend:** React Native, Expo (SDK 51), Expo Router (file-based routing)
- **State Management:** Zustand-based custom store architecture (`waterStore`, `goalStore`, `uiStore`)
- **Backend & Auth:** Firebase Authentication & Firestore (real-time database)
- **AI Layer:** Claude API integration for personalized lifestyle and sports-performance coaching
- **Build & Deployment:** EAS (Expo Application Services)

---

## 📥 Download & Install

Download the latest production-ready Android APK directly:

👉 **[Download AquaAI APK v1.0.0](YOUR_EXPO_DOWNLOAD_LINK_HERE)**

> ⚠️ **Note:** This build is signed with an ad-hoc local profile. You may need to enable **"Install from Unknown Sources"** in your Android settings to complete installation.

---

## 💻 Getting Started (Local Development)

### 1. Prerequisites
- [Node.js](https://nodejs.org/) (LTS recommended)
- npm or yarn
- [Expo Go](https://expo.dev/client) app (for testing on a physical device)

### 2. Clone & Install

```bash
git clone https://github.com/YOUR_GITHUB_USERNAME/aquaai.git
cd aquaai

# Install dependencies
npm install --legacy-peer-deps
```

### 3. Environment Setup

A `.env` file is already configured in the codebase with the required keys. If you're setting this up fresh, create a `.env` file in the project root with your own credentials:

```env
EXPO_PUBLIC_FIREBASE_API_KEY=your_firebase_key_here
EXPO_PUBLIC_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
EXPO_PUBLIC_FIREBASE_PROJECT_ID=your_project_id
EXPO_PUBLIC_FIREBASE_STORAGE_BUCKET=your_project.firebasestorage.app
EXPO_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
EXPO_PUBLIC_FIREBASE_APP_ID=your_app_id
EXPO_PUBLIC_GEMINI_API_KEY=your_gemini_key_here
```

### 4. Run the App

```bash
npx expo start --clear
```

Press **`a`** to launch on an Android emulator, or scan the QR code with the **Expo Go** app on your physical device.

---

## 📦 Native Cloud Build Process

This production build was compiled using **EAS (Expo Application Services)**:

```bash
# Generate native project files
npx expo prebuild --platform android

# Build the release APK via EAS Cloud
eas build -p android --profile preview
```

---

## 🗂️ Project Structure

```
AquaAI/
├── app/                        # Expo Router screens & navigation
│   ├── (auth)/                 # Login & password recovery
│   └── (tabs)/                 # Main tab screens (home, log, stats, AI coach, etc.)
├── assets/                     # App icons & splash images
├── docs/                       # Project documentation
├── src/
│   ├── components/
│   │   ├── ai/                 # AI Coach UI components
│   │   ├── charts/             # Data visualization (rings, bar charts, heatmaps)
│   │   ├── common/              # Shared UI kit (Button, Card, Input, Toast, etc.)
│   │   ├── layout/              # Header & screen wrappers
│   │   └── water/               # Water logging components
│   ├── constants/               # Static config (drinks, theme, tips)
│   ├── hooks/                   # Custom hooks (auth, water, sleep, steps, streak, etc.)
│   ├── services/
│   │   ├── api/                 # Claude API integration
│   │   └── firebase/            # Auth, Firestore, notifications
│   ├── store/                   # Zustand state stores
│   └── utils/                   # Helpers (dates, formatters, validators)
├── App.tsx
├── app.json
├── eas.json
└── index.ts
```

---

## 🗺️ Roadmap

- [ ] Weekly & monthly hydration insights dashboard
- [ ] Push notification reminders based on activity level
- [ ] Apple Health / Google Fit integration
- [ ] Social hydration challenges

---

## 👥 Contributors

**Saail Abbas** — Lead Software Engineer & Full-Stack Developer

Contributions are welcome! Feel free to open an issue or submit a pull request to help improve the architecture, fix bugs, or suggest new features.

---

## 📄 License

This project is licensed under the **MIT License** — feel free to use, modify, and distribute with attribution.

---

<p align="center">⭐ If you find this project useful, consider giving it a star on GitHub! ⭐</p>
