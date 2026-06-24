# ☕ Tea & Coffee Supply Manager
### From Excel Spreadsheet → Full Web Application

[![Version](https://img.shields.io/badge/Version-4.0-brown)](https://github.com/heysubu)
[![Excel](https://img.shields.io/badge/Microsoft-Excel-217346?logo=microsoft-excel)](https://github.com/heysubu)
[![HTML](https://img.shields.io/badge/Web%20App-HTML5-orange?logo=html5)](https://github.com/heysubu)
[![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla%20JS-yellow?logo=javascript)](https://github.com/heysubu)
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen)](https://github.com/heysubu)
[![Sponsor](https://img.shields.io/badge/❤️%20Sponsor-GitHub-pink?logo=github)](https://github.com/sponsors/heysubu)
[![Built with Claude](https://img.shields.io/badge/Built%20with-Claude%20AI-blueviolet)](https://claude.ai)

> 🚀 **A real-world example of converting an Excel tracking system into a working web application — no backend server needed. Just open the HTML file in any browser and it works!**

---

## 💡 The Story — Why This Was Built

Every corporate office has tea and coffee machines. Every month someone needs to track how much milk, coffee beans, tea premix, sugar, and stirrers were used — and by which company, from which vendor.

Before this project:
- Everything was tracked manually in Excel
- The file had to be shared back and forth by email
- Only one person could edit at a time
- No login, no access control — anyone could change anything
- No dashboard to see monthly trends

After this project:
- A web app that works in any browser
- Login screen with username and password
- Role-based access (Admin / Staff)
- Beautiful dashboard with KPI cards and charts
- Daily consumption entry with day-by-day tracking
- Export to CSV — import back into Excel anytime
- Print-ready A4 report with one click
- **No server needed — runs 100% in the browser**

---

## 📦 What's In This Repository

| File | What It Is |
|---|---|
| `Tea___Coffee_Supporting.xlsm` | The **original Excel file** — the data source with 5 sheets |
| `TeaCoffee_App_v4.html` | The **web application** — open in browser, works immediately |

> 💡 **How to use:** Download both files → Open the `.html` file in Chrome or Edge → Login with the credentials below → Start using the app!

---

## 🔐 Login Credentials

| Username | Password | Role | What They Can Do |
|---|---|---|---|
| `admin` | `admin123` | Admin 👑 | Full access to everything |
| `manager` | `mgr123` | Staff | Dashboard + Register (no Master Setup) |
| `staff` | `staff123` | Staff | Dashboard + Register (view only) |

---

## 📊 The Excel File — 5 Sheets Explained

The original Excel file (`Tea___Coffee_Supporting.xlsm`) has **5 sheets** that the web app is based on:

| # | Sheet Name | What It Contains |
|---|---|---|
| 1 | **DashBoard** | Monthly summary — company, vendor, item usage day-wise across 31 days |
| 2 | **Monthly Data** | Full transaction records — company, vendor, item, opening, order, usage amounts |
| 3 | **Validation** | Dropdowns — list of vendors, companies, items, and months |
| 4 | **Daily Data** | Day-by-day usage per item per company per vendor |
| 5 | **Pivot Chart** | Summary chart showing order vs usage by month |

**Companies tracked:** Office Space Con. · OWT Pvt Ltd · Digital Advice LLP

**Vendors tracked:** Sumant Technotrade · Veebha Beverages

**Items tracked (12 items):**
- Coffee Beans (₹700/Kg) · Coffee Beans Value Blend (₹720/Kg)
- Tea Premix 650ML · Coffee Premix 650ML (₹160 each)
- Sugar Sachet White (₹120/Kg) · Milk 1Ltr Good Life (₹69.52)
- Stirrer (₹0.26/Nos) · Flavor Tea Bags — Plain, Cardamom, Ginger, Masala (₹200–220/box)
- Lemon Green Tea Bags (₹4.50/Nos)

---

## ✨ Web App Features (v4.0)

### 📊 Dashboard Page
- **5 KPI Cards** — Opening Value · Order Value · Usage Value · Closing Value · Items Tracked
- **Bar Chart** — 4-month trend comparing orders vs usage visually
- **3 Filters** — Filter by Company, Vendor, and Month
- **Print A4** — One click prints the dashboard in landscape A4 format

### 📋 Consumption Register Page
- Select Month + Company + Vendor → full item register loads
- **Day-by-day entry** across 31 days for each item
- **Order entry section** (Admin only — staff cannot place orders)
- Save button with instant feedback toast notification
- Export individual month register as CSV

### ⚙️ Master Setup Page (Admin Only)
- **Vendors tab** — Add, edit, remove vendors
- **Items tab** — Full item master with name, unit, brand, HSN code, rate, vendor link
- **Companies tab** — Manage company list
- **Users tab** — Add users, assign Admin or Staff role, toggle individual permissions

### 🔐 Security & Access Control
- Login screen with username + password
- **Role-based permissions** — each user has individual permission switches:
  - Dashboard · Register · Master Setup · Sync · Consumption Entry · Orders
- All activity is logged (login, logout, exports, saves)
- Activity log visible to Admin in the Sync panel

### 🔄 Sync / Data Panel
- **Export CSV** — download all data as CSV file (named with timestamp)
- **Import CSV** — paste CSV data to restore or transfer data
- **CSV format shown** — so anyone can prepare data from Excel and import
- Activity log showing last 30 actions with user + timestamp

### 💾 Auto-Save (No Server Needed!)
- All data saved automatically to **browser localStorage**
- Data persists even after closing and reopening the browser
- No internet connection needed after initial load
- No backend, no database, no hosting required

---

## 🏢 Corporate Use Cases

This system is perfect for:

| Department | Use Case |
|---|---|
| **Facility Management** | Track tea/coffee consumption across all office floors |
| **Admin Team** | Monthly vendor billing — how much was ordered vs used |
| **Finance / Accounts** | Verify vendor invoices against actual consumption data |
| **Multiple Offices** | Each office is a different "Company" in the system |
| **Auditors** | Download monthly CSV and cross-check with purchase orders |
| **Managers** | View dashboard without editing — read-only access |

---

## 🔄 How Excel Became a Web App

This is the key learning of this project — here is how the conversion worked:

```
Excel File                    Web App
──────────────────────────────────────────────────────
DashBoard sheet         →     Dashboard page (KPI cards + chart)
Monthly Data sheet      →     Consumption Register page
Validation sheet        →     Dropdowns in all filters
Daily Data sheet        →     Day-by-day entry grid (31 columns)
Pivot Chart             →     Interactive bar chart (rendered with JS)
Data Validation         →     Dropdown menus with data validation
Password protection     →     Login screen + role-based permissions
VBA Macro buttons       →     HTML buttons with JavaScript functions
VLOOKUP formulas        →     JS filter functions on localStorage data
Print feature           →     Print A4 (CSS @media print)
Share via email         →     Share HTML file — works anywhere
```

**Technologies used in the Web App:**
- **HTML5** — Structure and layout
- **CSS3** — Styling, dark theme, responsive grid
- **Vanilla JavaScript** — All logic, calculations, data handling
- **localStorage** — Browser storage (replaces Excel file as data store)
- **Google Fonts** — Playfair Display + DM Sans for professional look
- **Claude AI (Anthropic)** — AI-assisted development (coding, debugging, refining)
- **No framework, no library, no server** — 100% self-contained single file

---

## 🚀 How to Use — 3 Simple Steps

**Step 1 — Download**
Download `TeaCoffee_App_v4.html` from this repository.

**Step 2 — Open**
Double-click the file → it opens in Chrome, Edge, or Firefox. No installation needed.

**Step 3 — Login & Use**
- Login with `admin / admin123`
- Go to **Master Setup** → add your companies, vendors, items
- Go to **Consumption Register** → select month → enter daily usage
- Go to **Dashboard** → see your KPIs and monthly trends
- Click **Print A4** to get a printable report

---

## 📋 How to Import Excel Data into the App

If you already have data in the Excel file, here is how to bring it into the web app:

1. Open the **Sync Panel** (click the 🔄 Sync button in the top bar)
2. Prepare your data in this CSV format:
```
month,company,vendor,item,order,day1,day2,...,day31
Jul-2024,Office Space Con.,Veebha Beverages,Tea premix,20,0,1,0,0,1,0,...
```
3. Paste it in the Import box → click Import
4. Data loads instantly into the app

---

## 🎬 App in Action

### 🔐 Login Page
<img width="1280" height="720" alt="☕ Tea   Coffee Manager - Brave 2026-05-16 21-29-36 fornt login page" src="https://github.com/user-attachments/assets/ebeec148-7eae-4977-8c45-34ada2c8888b" />

*Professional login screen — enter username and password to access the app. Each user sees only what their role allows.*

---

### 📋 Daily Consumption Entry
<img width="1280" height="720" alt="☕ Tea   Coffee Manager - Brave 2026-05-16 21-30-40Filling play" src="https://github.com/user-attachments/assets/4b0a2f6a-d177-49cb-8f63-452e2a8ce703" />

*Select month, company and vendor — then fill in daily usage for each item across 31 days. Totals calculate automatically.*

---

### ⚙️ Master Setup — Users & Permissions
<img width="1280" height="720" alt="☕ Tea   Coffee Manager - Brave 2026-05-16 21-31-28Master Setup" src="https://github.com/user-attachments/assets/f3bcfa8b-a88e-43b8-80e7-e3fc095ff0ab" />

*Admin panel for managing vendors, items, companies and users. Set individual permissions per user — who can view, enter data, or place orders.*

---

### 🔄 Sync Panel — CSV Export & Activity Log
<img width="1280" height="720" alt="☕ Tea   Coffee Manager - Brave 2026-05-16 21-32-30Sync" src="https://github.com/user-attachments/assets/e68d2a58-c98d-4a51-89c6-64c48c7f7799" />

*Export all monthly data as a timestamped CSV file. Import data from Excel. View the full activity log showing every action by every user.*

---

## 📂 Recommended Repository Structure

```
tea-coffee-supply-manager/
│
├── README.md                          ← This file
│
├── excel/
│   └── Tea___Coffee_Supporting.xlsm  ← Original Excel file
│
├── app/
│   └── TeaCoffee_App_v4.html         ← Web application (open in browser)

```

---

## 🤖 Built With Claude AI

> This project is a perfect example of **Human Creativity + AI Power** working together.

The web application (`TeaCoffee_App_v4.html`) was built with the help of **[Claude AI by Anthropic](https://claude.ai)** — one of the most advanced AI assistants available today.

Here is how it worked:

| What I Brought | What Claude AI Helped With |
|---|---|
| 💡 The idea — Excel to Web App | Writing the HTML structure |
| 📊 The Excel data model (5 sheets) | Building the JavaScript logic |
| 🏢 Real corporate use case knowledge | Designing the CSS layout & theme |
| 🔐 Role & permission requirements | Creating the login & access system |
| 📋 Feature requirements | Implementing localStorage auto-save |
| 🖨️ Print & export requirements | Building the CSV export/import system |
| ✅ Testing & reviewing every feature | Debugging and refining the code |

> 💬 **Key message:** AI did not build this project. **I designed it.** I knew what the problem was, I knew what features were needed, and I knew how the Excel data should map to a web app. Claude AI helped me write the code faster — just like how a calculator helps you calculate faster, but **you still need to know the math.**

**This is the future of work** — combining domain expertise and innovative thinking with AI tools to build things that would otherwise take weeks in just hours.

---

## 💡 Key Benefits

✅ **Zero cost** — No hosting, no server, no subscription

✅ **Works offline** — Open the HTML file without internet

✅ **Multi-user** — Different logins for Admin, Manager, Staff

✅ **Secure** — Role-based permissions per user

✅ **Audit trail** — All activity logged with user name and time

✅ **Print ready** — One click A4 landscape report

✅ **CSV bridge** — Connect web app data back to Excel anytime

✅ **Easy to customize** — One HTML file, easy to edit

✅ **Mobile friendly** — Works on tablet and phone browsers too

---

## 📄 License

MIT License — Free to use, share, and modify.

---

## 🌟 Project Stats

![GitHub stars](https://img.shields.io/github/stars/heysubu/tea-coffee-supply-manager?style=social)
![HTML](https://img.shields.io/badge/App-Single%20HTML%20File-orange?logo=html5)
![Excel](https://img.shields.io/badge/Source-Excel%20xlsm-217346?logo=microsoft-excel)
![Users](https://img.shields.io/badge/Users-3%20Role%20Types-blue)
![Items](https://img.shields.io/badge/Items-12%20Tracked-brown)
