# ⛪ FATIMA PARISH - GSK Tithes, Mortuary & Financial Management System

Sistema sa pagdumala sa mga Tithes (Ika-napulo), Mortuary (Abuloy sa Namatayan), GSK Community Allocations, ug Financial Reports alang sa **Our Lady of Fatima Parish**.

---

## 📁 Estruktura sa mga Files (File Directory Structure)

```text
SYSTEM ni maryjoy/
│
├── 📄 index.html              # Main Portal (Ang nag-unang website page sa tibuok sistema)
├── 📄 vercel.json             # Configuration file para sa Vercel.app hosting
├── 📄 README.md               # Kini nga guide (Deskripsyon sa tibuok sistema)
│
├── 📂 assets/                 # Folder sa mga Hulagway ug Logo
│   ├── logo.jpg               # Opisyal nga Logo sa Fatima Parish (Jubilaeum A.D. 2000)
│   └── logo_base64.txt        # Base64 data code sa logo para sa offline fallback
│
├── 📂 css/                    # Folder sa Design ug Styling
│   └── style.css              # Dashboard UI styles, themes, responsive layout, ug print styling
│
├── 📂 js/                     # Folder sa JavaScript (Mga Functions ug Logic sa Sistema)
│   ├── app.js                 # Role router, login handlers, navigation tabs, charts, ug modals
│   ├── data.js                # Database engine, LocalStorage caching, ug sample initial records
│   ├── tithes.js              # Kwentada sa Tithes, GSK 20%, Chapel 20%, ug Parish 60% shares
│   ├── mortuary.js            # Deceased registry, condolence contributions, ug financial aid
│   ├── settings.js            # Allocation percentages, system logs, export & import JSON backup
│   ├── logo-data.js           # Base64 logo data engine para sa offline ug sandboxed loading
│   └── supabase-config.js     # Cloud Database configuration (opsyonal para sa multi-device sync)
│
├── 📂 api/                    # Folder sa PHP REST API (Para sa MySQL / XAMPP hosting)
│   ├── config.php             # Database connection settings
│   ├── auth.php               # Login & authentication API
│   ├── members.php            # Member management API
│   ├── tithes.php             # Tithes records API
│   ├── mortuary.php           # Mortuary records API
│   ├── expenses.php           # Chapel expenses API
│   ├── deceased.php           # Deceased registry API
│   ├── logs.php               # System audit logs API
│   ├── settings.php           # Parish settings API
│   └── status.php             # Server health check API
│
└── 📂 database/               # Folder sa Database Schemas & SQL Scripts
    ├── fatima_parish_db.sql   # SQL schema para sa MySQL / phpMyAdmin
    └── supabase_schema.sql    # SQL schema para sa Cloud Supabase Database
```

---

## 🔑 Default Login Credentials

| Role | Username / Email | Password | Assigned Scope / Access |
|---|---|---|---|
| **Secretary** | `sec_juan` o `secretary.fatimaparish@gmail.com` | `password123` | Tibuok Parokya, Members, Tithes, Mortuary, Settings, ug Printing |
| **GSK Leader 1** | `gsk_leader_1` o `gsk.sanjose@gmail.com` | `leader123` | **GSK San Jose** (Records, Tithes, Mortuary) |
| **GSK Leader 2** | `gsk_leader_2` o `gsk.santamaria@gmail.com` | `leader123` | **GSK Santa Maria** (Records, Tithes, Mortuary) |
| **GSK Leader 3** | `gsk_leader_3` o `gsk.sanpedro@gmail.com` | `leader123` | **GSK San Pedro** (Records, Tithes, Mortuary) |
| **GSK Leader 4** | `gsk_leader_4` o `gsk.santorosario@gmail.com` | `leader123` | **GSK Santo Rosario** (Records, Tithes, Mortuary) |
| **Parishioner** | *1-Click Direct Access* | *Walay Password* | Public Financial Transparency & Tithes Reports |

---

## 🚀 Giunsa Pag-Host (Hosting Guide)

### 1. Pag-Host sa Vercel (Libre & Paspas)
1. I-upload ang tibuok folder sa imong **GitHub Repository**.
2. Adto sa **[vercel.com](https://vercel.com)** $\rightarrow$ I-import ang repository $\rightarrow$ I-click ang **Deploy**.
3. Automatic kining mahatagan og live link sama sa `https://fatima-parish.vercel.app`.

### 2. Pag-Balhin sa Data gikan sa Local ngadto sa Online Link
1. **Sa Local Computer:** Log in isip **Secretary** $\rightarrow$ Adto sa **Settings** $\rightarrow$ I-click ang **Export Database Backup** (ma-download ang JSON file).
2. **Sa Vercel Website:** Log in isip **Secretary** $\rightarrow$ Adto sa **Settings** $\rightarrow$ I-click ang **Import Database Backup** $\rightarrow$ Pilia ang na-download nga JSON file.
3. Ang tanang data parehas na 100% sa local ug online!
