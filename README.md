# TrustLoop 🛡️
### AI-Powered Dual Trust Ecosystem for Delivery Workers
> *"Uber rates drivers. Amazon rates sellers. Nobody rates customers. We do — and we make it count for insurance."*

---

## 🚨 The Problem

Meet **Ravi**, 28, a Zomato delivery partner in Chennai.

- He has been delivering for **3 years** with a near-perfect record
- He pays a **fixed weekly premium** even on days he earns nothing
- Two angry customers gave him **unfair 1-star ratings** — his premium went up with no appeal
- When he got injured, his **claim took 4 weeks** to process
- He enters dangerous addresses and flooded roads with **zero warning**
- He is **completely alone** — no community, no support, no voice

**50 million gig workers in India face this exact situation. No insurance product solves it.**

---

## 💡 Our Solution — TrustLoop

TrustLoop is the world's first **AI-powered dual trust ecosystem** for delivery workers.

Both the **delivery worker** AND the **customer** get a continuous AI trust score — and that combined score determines insurance premiums, claim speed, delivery matching, and rewards.

---

## 👥 Persona-Based Scenarios

### Persona 1 — Ravi (Delivery Worker)
- TrustScore: 847 → Shield Rank: Gold
- Weekly premium: ₹15 (down from ₹90 when he started)
- Files a claim with one photo → jury of 7 fellow workers approves in 8 minutes → money in account in 47 minutes
- Gets anonymous danger alert before reaching a risky address → coverage auto-upgrades to protect him

### Persona 2 — Priya (Customer)
- TrustScore: 920 → Priority customer
- Always gets the best available worker assigned first
- Her fair rating history means her reviews carry more weight in the system
- Gets instant refund protection because her trust history proves she doesn't abuse it

### Persona 3 — Insurer / Underwriter (Guidewire)
- Gets the most accurate real-world risk dataset ever built — from 50 million deliveries
- Community danger alerts feed directly into zone-level risk pricing
- Fraud is pre-screened by AI before any human reviews it
- High-trust worker pools cost less to insure — actuarially defensible pricing

---

## ⚙️ How the Workflow Works

```
Worker opens app
      ↓
Sees TrustScore + Shield Rank + Danger Alerts
      ↓
Activates shift → Coverage goes live
      ↓
Delivers orders → AI scores every micro-signal
      ↓
Incident happens → Files claim with 1 photo
      ↓
AI fraud pre-screen → Passes to 7-worker jury
      ↓
Jury votes in 10 minutes → Approved
      ↓
Guidewire PolicyCenter processes payout
      ↓
Money in wallet in under 1 hour
```

---

## 🤖 How the AI Trust Score Works

### Worker Trust Score (signals used)
| Signal | Weight |
|--------|--------|
| Customer ratings (bias-adjusted) | High |
| On-time delivery streak | High |
| Safe driving behaviour | High |
| Zero complaint history | Medium |
| Years on platform | Medium |
| Community vouches received | Medium |
| Package handling care | Low |

### Customer Trust Score (signals used)
| Signal | Weight |
|--------|--------|
| Fairness of ratings given to workers | High |
| False complaint history | High |
| Availability at delivery address | Medium |
| Payment reliability | Medium |
| Accurate address inputs | Medium |
| Respectful behaviour reports | Low |

### Smart Matching Engine
When a delivery is assigned, both scores combine into a **Delivery Trust Index**:

| Worker Score | Customer Score | Outcome |
|---|---|---|
| High (850+) | High (850+) | Zero premium for worker. Priority delivery for customer. Both earn bonus points |
| High (850+) | Low (below 400) | Worker's coverage auto-upgrades BEFORE they reach the address |
| Low | High | Best learning environment — high-trust customer assigned to help new worker build score |
| Both low | Both low | AI nudges sent to both with specific improvement actions |

---

## 💸 Weekly Premium Model

| Shield Rank | Trust Score | Weekly Premium | Coverage | Claim Speed |
|---|---|---|---|---|
| 🏆 Legend | 900–1000 | ₹0 (zero) | ₹5,00,000 | AI auto < 5 min |
| 🥇 Gold | 750–899 | ₹15/week | ₹3,00,000 | FastTrack < 30 min |
| 🥈 Silver | 550–749 | ₹35/week | ₹2,00,000 | Jury < 2 hours |
| 🥉 Bronze | 350–549 | ₹60/week | ₹1,00,000 | Standard < 24 hrs |
| 🆕 New | 0–349 | ₹90/week | ₹50,000 | Standard < 48 hrs |

### Parametric Triggers (automatic — no worker action needed)
- 🌧️ Rain or storm alert in worker's zone → coverage auto-upgrades one tier
- 🚨 Worker enters community-flagged danger zone → premium coverage activates instantly
- 🌙 Worker works past midnight → night-shift rider automatically activated
- 💸 Earnings drop below ₹200 for 3 consecutive days → premium paused, basic cover maintained
- ✅ 3 consecutive days with zero complaints → +10 trust points bonus

---

## 🧠 AI/ML Plan

### Model 1 — Trust Score Prediction Engine
- **Algorithm:** XGBoost Gradient Boosting
- **Input:** 47 behavioural micro-signals per worker, 31 signals per customer
- **Output:** Trust score 0–1000, updated after every delivery
- **Key innovation:** Single ratings are unreliable. Patterns over 50+ deliveries are highly predictive of future risk. Statistical outlier detection removes biased ratings automatically.

### Model 2 — Fraud Detection
- **Algorithm:** Isolation Forest anomaly detection
- **Checks:** GPS location vs reported accident location, accelerometer data vs claimed injury type, timing patterns, network analysis for coordinated fraud rings
- **Output:** Fraud probability score 0–100 shown to jury before voting

### Model 3 — Smart Delivery Matching
- **Algorithm:** Collaborative filtering + contextual bandits
- **Input:** Worker trust score + customer trust score + weather + time + zone risk
- **Output:** Optimal worker-customer match that minimises risk for both sides

### Model 4 — Danger Zone Clustering
- **Algorithm:** DBSCAN spatial clustering on anonymous worker alerts
- **Output:** Real-time danger heatmap fed directly into Guidewire as zone-level risk data

---

## 📱 Platform Choice — Mobile PWA

We chose **Mobile-first Progressive Web App** because:
- Delivery workers use smartphones exclusively — desktop is irrelevant
- Works on low-end Android devices (₹6,000–₹12,000 phones)
- Offline-first — trust score and danger alerts cached locally, sync when connectivity returns
- No app store approval needed — workers install directly from browser
- Push notifications work natively — danger alerts delivered even when app is closed

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React Native (Expo) |
| UI | TailwindCSS + Shadcn |
| Backend | FastAPI (Python) |
| Database | PostgreSQL + Redis |
| ML Models | scikit-learn, XGBoost |
| Real-time | WebSockets (Socket.io) |
| Maps | Mapbox GL JS |
| Insurance Engine | Guidewire PolicyCenter API |
| Auth | Firebase Auth |
| Hosting | AWS (EC2 + RDS + S3) |

---

## 📅 Development Plan

### Phase 1 (March 4–20) — Ideation & Foundation ✅
- [x] Worker trust score dashboard
- [x] Customer trust score system
- [x] Basic smart matching prototype
- [x] Community pool visualization
- [x] Anonymous danger alert (one-tap send & receive)
- [x] Guidewire PolicyCenter basic integration

### Phase 2 (March 21–April 4) — Automation & Protection
- [ ] Full peer jury voting system
- [ ] Fraud detection ML model (live)
- [ ] FastTrack claim filing (one photo, AI decision < 5 min)
- [ ] Parametric trigger automation (weather API)
- [ ] Full payout automation via Guidewire (< 1 hour)

---

## 🎬 Demo Video
[▶️ Watch our 2-minute prototype walkthrough](#) ← *paste your YouTube link here*

---

## 📁 Repository Structure

```
TrustLoop/
├── README.md
├── trustloop-app/        # React Native frontend
├── trustloop-api/        # FastAPI backend + ML endpoints
├── ml-models/            # XGBoost, Isolation Forest, matching engine
├── guidewire-integration/ # PolicyCenter API layer
└── docs/                 # Architecture diagrams + wireframes
```

---

## 🌍 Why TrustLoop Wins

- **World first:** No product anywhere gives customers a trust score in a delivery ecosystem
- **AI-predictive:** Warns before problems happen — not after
- **Fair:** Bias removal protects workers from unfair ratings
- **Guidewire-native:** PolicyCenter is the engine. TrustLoop is the community intelligence layer
- **Massive scale:** 50 million gig workers in India. 300 million globally.

---

*Guidewire DEVTrails University Hackathon 2026 — Phase 1 Submission*
