# FocusSense: Intelligent Study Behavior Analyzer 🧠⏳

**FocusSense** is a professional-grade Android productivity ecosystem designed to transform the smartphone from a source of distraction into a disciplined "Deep Work" laboratory. Unlike traditional Pomodoro timers that rely on user honesty, FocusSense uses system-level monitoring and behavioral AI to enforce accountability and optimize cognitive performance.

---

## 🚀 Key Features

### 🛡️ Enforced Accountability (Penalty System)
*   **Active Distraction Tracking:** Utilizes the Android `UsageStatsManager` to detect when a user leaves the app to check social media or games during a session.
*   **Real-time Penalty:** Automatically appends a **+5 minute penalty** to the active timer if a distraction is detected, creating a psychological deterrent against procrastination.
*   **Motivational UI:** Displays dynamic quotes and warnings upon returning to the app to refocus the user's mindset.

### 🎧 Auditory Flow System
*   **Lifecycle-Aware Soundscapes:** Integrated player featuring curated ambient audio (**Rain, Zen, Lo-Fi, White Noise**) to help users enter a flow state.
*   **Scientific Transitions:** A custom **10-second auditory bridge** (Clock Ticking to Soft Bell) that prepares the brain for the transition from work to rest.
*   **Custom Playlists:** Supports local device storage integration, allowing users to build their own study soundtracks.

### 🤖 Heuristic AI Analytics
*   **Focus Score (0–100):** A data-driven metric calculated for every session by analyzing the ratio of completed work vs. distraction frequency.
*   **Behavioral Personas:** Clusters users into profiles such as **"Deep Worker"**, **"Night Owl"**, or **"Distracted Learner"**.
*   **Prime Focus Hour:** Predicts the exact hour of the day when the user is naturally most productive based on historical trends.

### 📊 Visual Dashboard
*   **Trend Analysis:** Uses **MPAndroidChart** to visualize focus consistency and improvement over days and weeks.
*   **Explainable AI Insights:** Translates complex behavioral data into actionable study coaching tips.

---

## 🛠️ Technical Stack

*   **Language:** 100% Kotlin
*   **Architecture:** Clean Architecture (UI, Logic, Data, Domain) with **MVVM**
*   **UI Framework:** Material Design 3, ViewBinding, Jetpack Navigation
*   **Data Persistence:** Moshi (JSON Serialization) + SharedPreferences
*   **System APIs:** Android `UsageStatsManager` (Tracking), `MediaPlayer` (Audio)
*   **Libraries:** 
    *   `MPAndroidChart` (Data Visualization)
    *   `Kotlin Coroutines` (Asynchronous Logic)
    *   `Moshi` (JSON handling)

---

## 📂 Project Structure
FocusSense
├── app
│   ├── src/main/java/com/sahana/focussense
│   │   ├── ui/               # Presentation Layer (Fragments & ViewModels)
│   │   │   ├── TimerFragment.kt      # Core Pomodoro & Penalty Logic
│   │   │   ├── MusicFragment.kt      # Ambient Audio Interface
│   │   │   ├── DashboardFragment.kt  # Progress Visualization
│   │   │   └── InsightsFragment.kt   # AI Behavioral Reports
│   │   ├── logic/            # Business Logic & AI Engine
│   │   │   ├── FocusAnalyzer.kt      # Heuristic Scoring & Clustering
│   │   │   └── DistractionTracker.kt # UsageStatsManager Integration
│   │   ├── music/            # Auditory Lifecycle Management
│   │   │   └── MusicManager.kt       # Audio Threading & Playlist Logic
│   │   ├── data/             # Persistence & Repository
│   │   │   └── SessionRepository.kt  # JSON Serialization (Moshi)
│   │   └── models/           # Domain Entities
│   │       └── SessionRecord.kt      # Data Schema for Focus Events
│   └── src/main/res/
│       ├── raw/              # Audio Assets (Ambient Sounds & Bells)
│       ├── layout/           # Cyberpunk-themed XML UI Designs
│       └── navigation/       # Jetpack Navigation Graph
├── build.gradle.kts          # Project-level Configuration
└── README.md                 # Project Documentation


---

## 🌍 SDG Alignment
FocusSense is mapped to the **United Nations Sustainable Development Goals**:
*   **SDG 4 (Quality Education):** Enhancing learning efficiency through data-driven habit analysis.
*   **SDG 3 (Good Health & Well-being):** Promoting digital well-being and reducing cognitive stress through auditory therapy.

---

## 📦 Installation & Execution

1.  **Clone the Repository:**
    git clone https://github.com/sahanawpt/FocusSense.git

2.Replace Placeholder Audio: Navigate to app/src/main/res/raw/ and replace the placeholder MP3 files with real audio files (ensure filenames match: rain.mp3, zen.mp3, lofi.mp3, timer_end.mp3).
3.Grant Permissions: Upon first launch, the app will request Usage Access. This is required for the penalty system to detect distractions.
4.Build & Run: Open in Android Studio, sync Gradle, and run on a physical device (API 26+) for the best experience.

---
📜 Future Scope
•
Gamification: Leveling system and "Focus RPG" elements to reward consistency.
•
Group Mode: Synchronized study rooms with shared accountability features.
•
Cloud Sync: Firebase integration for cross-device tracking and data backup.











---
👨‍💻 Author
Sahana S
Portfolio Project for Intelligent Study Behavior Analysis
FocusSense is not just a timer—it is a laboratory for mastering your own cognitive habits
