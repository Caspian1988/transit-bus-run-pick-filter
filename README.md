# 🚌 Ride On Bus Run Pick Filter & Pay Calculator

> An interactive shift-bidding optimizer, schedule visualizer, and gross payroll calculator designed for municipal transit operators.

[![Live Demo](https://img.shields.io/badge/Demo-Live%20Bid%20Filter-blue?style=for-the-badge&logo=github)](https://caspian1988.github.io/transit-bus-run-pick-filter/)

---

## 📋 The Problem It Solves

During quarterly or semi-annual transit system sign-ups (bids/picks), bus operators are handed thick packets containing dozens of candidate work schedules. Operators must quickly balance competing priorities under strict time limits:
- **Shift Structure**: Straight runs vs. Split runs (with midday unpaid spreads)
- **Workweek Length**: Standard 5-day schedules vs. compressed 4-day (10-hour) workweeks
- **Rest Days**: Desirable weekend combinations (Sat-Sun, Sun-Mon, Fri-Sat) or 3-day blocks
- **Financial Impact**: How built-in weekly overtime (hours over 40) translates to gross weekly and annual pay

Filtering through paper rosters or static PDFs is slow, error-prone, and stressful. **This application digitizes the entire bid sheet**, letting operators search, filter, compare, and instantly project their earnings with zero guesswork.

---

## 🚀 Live Demo

Test the live application directly in your browser:  
🔗 **[Ride On Bid Filter & Pay Calculator](https://caspian1988.github.io/transit-bus-run-pick-filter/)**

---

## ✨ Key Features

### 🔍 1. Multi-Criteria Shift Filtering & Sorting
- **Keyword Search**: Instant search by Pick number, Run ID, or shift notes.
- **Shift Types**: Filter by **Straight Run**, **Split Run**, **4-Day Workweek**, or **PM Shift**.
- **Days Off Matching**: Filter for **Sat-Sun**, **Sun-Mon**, **Fri-Sat**, or **3 Consecutive Days Off**.
- **Threshold Filters**: Filter by minimum guaranteed weekly pay hours.
- **Smart Sorting**: Order picks by Pick Number, Highest Weekly Pay, Earliest Report Time, or Earliest Off Time.

### 📅 2. Comprehensive Schedule Cards
- Day-by-day weekly breakdown (Sunday through Saturday).
- Highlights on/off duty times, individual run numbers, and daily pay allocations.
- Clear visual tagging for **OFF** days.
- Color-coded badges for quick identification of split, straight, and 4-day schedules.

### 💰 3. Floating Overtime & Payroll Calculator
- **1-Click Sync**: Click `Calculate Pay ⚡` on any pick card to automatically push its exact weekly pay hours into the calculator widget.
- **Earnings Breakdown**:
  - Calculates base hourly wage from annual step salary ($Salary / 2080$).
  - Automatically isolates straight time (up to 40 hrs) and overtime ($1.5\times$ base rate for hours $> 40$).
  - Projects both **Gross Weekly Earnings** and **Gross Annualized Earnings**.
- **Collapsible Drawer**: Floating widget can be minimized to stay out of the way while browsing runs.

### 📌 4. Interactive Comparison Dock
- Pin multiple candidate picks using the **Compare** checkbox.
- A persistent bottom dock keeps your shortlisted picks visible across searches so you can make your final bidding decisions side-by-side.

---

## 🧮 Payroll Logic & Formulas

The integrated calculator uses standard municipal transit payroll conventions:

$$\text{Base Hourly Rate} = \frac{\text{Annual Base Salary}}{2080\text{ hours}}$$

$$\text{Straight Pay} = \min(\text{Weekly Hours}, 40) \times \text{Base Hourly Rate}$$

$$\text{Overtime Pay} = \max(0, \text{Weekly Hours} - 40) \times (\text{Base Hourly Rate} \times 1.5)$$

$$\text{Gross Weekly Earnings} = \text{Straight Pay} + \text{Overtime Pay}$$

$$\text{Gross Annual Earnings} = \text{Gross Weekly Earnings} \times 52$$

---

## 🛠️ Built With

- **HTML5 & CSS3**: Custom CSS Variables, Flexbox, and CSS Grid with responsive design.
- **Vanilla JavaScript**: High-performance client-side filtering, state management, and real-time DOM manipulation (zero framework dependencies).
- **Typography**: Optimized readability with `JetBrains Mono` for tabular timings and `Oswald` for high-impact metric headers.
- **Deployment**: Hosted directly via GitHub Pages.

---

## 💻 How to Run Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/caspian1988/transit-bus-run-pick-filter.git
