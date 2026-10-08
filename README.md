# CAMPUSSHIELD AI
> **“Detect Early. Respond Fast. Keep Campus Safe.”**

CampusShield AI is an intelligent emergency coordination and campus safety platform designed for universities and colleges. It bridges students, faculty, campus safety officers, and institutional administrators with early detection, accessible emergency beacons, privacy-first analytics, and offline-resilient reporting.

---

## 🛡️ Critical Safety & Ethical Mandates

1. **Coordination System, Not Emergency Service Replacement:**
   CampusShield AI is an emergency coordination and information system, **NOT** a substitute for police, ambulance, fire services, doctors, or campus security personnel. In active life-threatening emergencies, dial **112 / 108 / 101** directly.
2. **Human Verification Required:**
   The system never automatically dispatches emergency services or declares emergencies solely from AI predictions. Human authorized responders verify alerts before escalation.
3. **Transparent AI Estimates:**
   AI-generated priority suggestions and risk scores are transparently explained with rationale and confidence estimates. Human responders can override suggestions anytime.
4. **Student Privacy Protection:**
   Individual student GPS coordinates and personal identities are **never** displayed publicly. All maps, check-ins, and analytics aggregate data anonymously.
5. **Zero-Profiling Ethics:**
   The AI Pattern Engine analyzes **only** aggregated campus infrastructure, environmental reports, and temporal clusters. It never labels individuals as dangerous or predicts crime by specific people.
6. **Graceful Offline & Demo Mode:**
   When offline, the system queues non-sensitive draft reports locally, clearly stating alerts are queued rather than falsely claiming delivery. Simulated drill features are prominently watermarked: `SIMULATION – NOT A REAL EMERGENCY`.

---

## 🌟 Core Features Overview

| Feature | Description |
|---|---|
| **1. One-Tap Emergency Assistance** | Rapid two-step confirmation beacon covering 7 categories (Medical, Fire, Security/Safety, Accident, Natural disaster, Harassment/threat, Other) with opt-in approximate location and optional photo. |
| **2. Smart AI Emergency Reporting** | Natural language report parser extracting category, location, urgency level, keywords, and follow-up safety questions with human verification disclaimer. |
| **3. Interactive Campus Safety Map** | Interactive Leaflet/OSM map detailing Help Points (Blue Lights), Security Offices, First-Aid/AEDs, Fire Equipment, Exits, Muster Points, Accessible Ramps, Safe Zones, and Hazards with a "Find Nearest Safe Point" locator. |
| **4. Hazard & Incident Reporting** | Non-emergency maintenance reporting (Broken street lights, leaks, pathway damage, etc.) with community corroboration upvoting and a 4-step resolution pipeline. |
| **5. AI Safety Pattern Analysis** | Administrator-restricted analytics analyzing 150+ historical reports into zone clusters, repeated infrastructure bottlenecks, and time-of-day distributions. |
| **6. Emergency Response Dashboard** | Live triage board for authorized responders to accept alerts, assign units, log field notes, transition statuses, and override priorities. |
| **7. Smart Alert Prioritization** | Transparent rule + NLP scoring engine (CRITICAL, HIGH, MEDIUM, LOW) detailing exact reasons for priority suggestions. |
| **8. Campus Broadcast System** | Administrator verified emergency broadcasts (Severe weather, closures, power/water, evacuation) with targeted campus zone scoping and audio read-aloud. |
| **9. Emergency Check-In** | One-tap *"I'm Safe"* and *"I Need Assistance"* roll-call with aggregate community counts and private responder queue. |
| **10. Accessibility Emergency Mode** | High-contrast black/yellow mode, large touch targets, screen-reader ARIA tags, plain-language guides, and multilingual support in **English, Kannada (ಕನ್ನಡ), and Hindi (हिन्दी)**. |
| **11. Offline / Poor-Connection Resilience** | Automatic network detection, manual offline simulator, LocalStorage queueing, and automatic server synchronization upon reconnection. |
| **12. Emergency Preparedness Hub** | Short, accessible guides on Fire Safety (P.A.S.S.), Earthquakes, Floods, First-Aid/AED, Evacuation, Electrical, Cyber Safety, and interactive checklist. |
| **13. Drill / Training Simulation Mode** | Safe simulation mode with timer, simulated participant counters, muster compliance metric, and siren audio test with zero false emergency dispatches. |
| **14. Response Audit Timeline** | Detailed step-by-step chronology for every incident (*Reported → Received → Verified → Assigned → Response Started → Resolved*). |
| **15. Campus Community Safety Score** | Metric-driven institutional safety index (Score: 91/100, Grade A+) tracking dispatch velocity, hazard resolution, and zone health. |

---

## 🚀 Getting Started

### Prerequisites
- **Node.js** v18+ (tested on Node v24)
- **npm** v9+

### Directory Structure
```
campusshield-ai/
├── client/                 # React 19 + TypeScript + Vite + Tailwind CSS v4 + Leaflet
│   ├── src/
│   │   ├── components/     # 15 Core Feature Components + Modals + Navigation
│   │   ├── types/          # Strict TypeScript interfaces
│   │   ├── utils/          # Offline storage, sound synthesis, translations (EN/KN/HI)
│   │   ├── App.tsx         # Main master view & tab routing
│   │   └── main.tsx
│   ├── package.json
│   └── vite.config.ts      # Proxy to backend on port 5000
│
└── server/                 # Node.js + Express REST API
    ├── src/
    │   ├── ai/             # Keyword extraction & aggregated pattern recognition engine
    │   ├── data/           # Mock database, 150+ historical reports, contacts, safety scores
    │   └── index.js        # REST endpoints & server boot
    └── package.json
```

### Running the Application

1. **Start the Backend Server (Port 5000):**
   ```bash
   cd server
   node src/index.js
   ```

2. **Start the Frontend Client (Port 3000):**
   ```bash
   cd client
   npm run dev
   ```

3. **Open in Browser:**
   Visit `http://localhost:3000/`

---

## 👥 Role-Based Access Control (RBAC)

The top navigation bar includes an instant role switcher to test all user perspectives:
- **Student**: Submit emergency alerts, report non-emergency hazards, check-in as safe, access campus map, view broadcasts.
- **Staff**: Department-level hazard submission and emergency assistance requests.
- **Security Responder**: Dispatch triage dashboard, incident assignment, status progression, field note logging, priority overriding.
- **Administrator**: Full dispatch privileges, verified campus broadcast issuance, drill simulation launcher, and AI Pattern Analytics.

