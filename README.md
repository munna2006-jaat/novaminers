# ⛏️ NovaMiners - Global Cloud Mining & VIP Staking Platform

**NovaMiners** is an ultra-luxury, high-yield decentralized ASIC cloud mining & VIP investment platform with a real-time web portal, live earnings countdown engine, multi-QR dynamic payment gateway, lucky wheel rewards, and automated administrative settlement dashboard.

---

## 🔐 Admin Panel Credentials

Access the executive administrative portal to manage users, ASIC mining plans, deposits, multi-QR pool, and payout receipts:

- **Admin Portal URL**: `/admin` (or `https://your-app.onvoroa.com/admin`)
- **Admin Username**: `Nova_MasterAdmin`
- **Admin Password**: `NovaMine@2026#VaultAdmin!`

> **Security Note**: You can also update these credentials anytime inside `data/db.json` or by setting environment variables `ADMIN_USER` and `ADMIN_PASS`.

---

## 🚀 How to Deploy on Voroa (app.getvoroa.com)

Deploying NovaMiners on Voroa takes less than 2 minutes. The project uses lightweight standard Node.js without any C++ native module dependencies (no segmentation fault risks).

### Step-by-Step Voroa Deployment:

1. **Open Voroa Dashboard**:
   - Visit [app.getvoroa.com](https://app.getvoroa.com) and sign in.
2. **Create New Web Service**:
   - Click **"+ New Service"** or **"Create Service"** -> Choose **"Web Service"**.
3. **Connect GitHub Repository**:
   - Select **GitHub** as the source provider.
   - Choose repository: **`munna2006-jaat/novaminers`** (Branch: `main`).
4. **Service Configuration Settings**:
   - **Service Name**: `novaminers` (or any preferred name)
   - **Environment / Runtime**: `Node.js` (Node 18+ or 20+)
   - **Build Command**: `npm install`
   - **Start Command**: `npm start`
   - **Port**: `3000` *(Voroa binds to `process.env.PORT` automatically)*
5. **Environment Variables (Optional)**:
   - If you want custom admin credentials via environment, set:
     - `PORT` = `3000`
     - `ADMIN_USER` = `Nova_MasterAdmin`
     - `ADMIN_PASS` = `NovaMine@2026#VaultAdmin!`
6. **Click "Deploy"**:
   - Voroa will clone the repo, run `npm install`, and launch `server.js`.
   - Once deployment status turns green (**Live / Active**), click on the provided URL (e.g. `https://novaminers.onvoroa.com`).
7. **Access Admin Portal**:
   - Open `https://novaminers.onvoroa.com/admin`
   - Login with `Nova_MasterAdmin` and `NovaMine@2026#VaultAdmin!`.
   - Update your Merchant UPI ID, QR code rotation images, and Telegram channel link in Settings.

---

## 🌟 Key Platform Features

- **📱 Ultra-Luxury Mobile-First UI**: Golden & obsidian theme with smooth animations, tabs, and wallet overview.
- **⚡ 45-Minute Quick Mining Yield**: ASIC mining contracts automatically credit hourly and daily yield to user balances.
- **🔄 Dynamic Multi-QR Auto-Rotation Pool**: Add unlimited merchant QR codes with rotation timers, round-robin allocation, and active status control.
- **🧾 High-Definition Payout Receipt Generator**:
  - Download crisp 2.5x HD PNG receipts for bank/UPI payouts.
  - One-click copy formatted Telegram / WhatsApp payout proofs for channel announcements.
  - Print receipt directly from the admin panel.
- **🎁 Daily Attendance & Lucky Spin Wheel**: Daily bonus check-in and interactive spinning wheel for miner retention.
- **🛡️ 100% Reliable JSON Engine**: No native binary build steps needed during deployment, guaranteeing zero crash deployments.

---

## 💻 Local Development Setup

```bash
# 1. Clone the repository
git clone https://github.com/munna2006-jaat/novaminers.git
cd novaminers

# 2. Install dependencies
npm install

# 3. Start development server
npm start

# 4. Open in browser
# Client Portal: http://localhost:3000
# Admin Dashboard: http://localhost:3000/admin
```

---

## 📁 Project Architecture

```
novaminers/
├── data/
│   └── db.json             # Persistent JSON database (users, plans, qr pool, admin credentials)
├── public/
│   ├── admin.html          # Full-featured Executive Admin Portal & Settlement Desk
│   ├── index.html          # Client SPA (Mining plans, wallet, attendance, team referral)
│   ├── css/
│   │   └── style.css       # Obsidian & Gold Luxury Theme
│   ├── js/
│   │   └── app.js          # Client-side reactivity, countdown timers, UPI payment deep-linking
│   └── images/             # Mining rig SVG assets & crypto coin badges
├── server.js               # Express 5 API backend & cloud miner daemon
├── package.json            # Project manifest & dependencies
└── README.md               # Documentation & deployment instructions
```

---

© 2026 **NovaMiners Global Network**. All rights reserved.
