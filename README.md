# EduCore — School Management System

> A fully functional, single-file HTML prototype for school administration. Built with vanilla HTML, CSS, and JavaScript — no frameworks, no backend required.

---

## Overview

EduCore is a modern school management system prototype designed to demonstrate a complete admin panel UI to school principals, teachers, or stakeholders before actual development begins. Everything runs in a single `.html` file that you can open in any browser.

---

## Features

### Sections Included

| # | Section | Key Features |
|---|---------|--------------|
| 1 | **Dashboard** | Stat cards, activity feed, upcoming events, attendance chart, fee summary, top performers |
| 2 | **Student Management** | Searchable/filterable table, add student modal, clickable profile modals |
| 3 | **Teacher Management** | Teacher table with subject & class assignments |
| 4 | **Classes & Subjects** | Class overview, section management, subject allocation |
| 5 | **Attendance** | Daily attendance sheet with Present / Absent / Late toggles, monthly summary cards |
| 6 | **Assignments** | Assignment table with due dates and submission status |
| 7 | **Exams & Results** | Exam schedule, marks sheet, result summary cards, ranking table |
| 8 | **Fee Management** | Fee collection table, Paid/Pending/Overdue badges, revenue summary cards |
| 9 | **Reports & Analytics** | Attendance trend chart, performance chart, fee collection chart |
| 10 | **Notifications** | School announcements, exam reminders, homework reminders |

---

## Getting Started

### Requirements

- Any modern web browser (Chrome, Firefox, Edge, Safari)
- No server, no Node.js, no installation required

### Running the Prototype

1. Download `school_management_system.html`
2. Double-click the file to open it in your browser

That's it. The entire system runs locally in your browser.

---

## Project Structure

Since this is a single-file application, all code lives in `school_management_system.html`:

```
school_management_system.html
├── <head>
│   ├── Google Fonts (DM Sans + DM Serif Display)
│   ├── Font Awesome 6.5 (icons)
│   └── <style> — All CSS (variables, layout, components)
│
├── <body>
│   ├── Sidebar navigation
│   ├── Top header / navbar
│   ├── Page sections (10 sections, shown/hidden via JS)
│   └── Modals (Add Student, Student Profile)
│
└── <script>
    ├── Sample data arrays (students, teachers, classes, fees, etc.)
    ├── Render functions (populate tables and lists dynamically)
    ├── Navigation logic (section switching)
    ├── Sidebar toggle (desktop collapse + mobile drawer)
    ├── Modal open/close
    ├── Attendance toggle buttons
    └── Table search/filter
```

---

## Sample Data Included

The prototype ships with realistic dummy data so it looks like a live system:

- **15 students** with names, IDs, classes, parent contacts, and fee status
- **8 teachers** with subject and class assignments
- **4 grade levels** (9–12) with sections A, B, C
- **8 subjects** with codes, teachers, and type (Core / Elective)
- **30 students** in the attendance daily sheet
- **7 assignments** with submission counts and due dates
- **6 exam schedule entries**
- **10 student rankings** with marks and grades
- **7 student marks sheets** across 6 subjects
- **11 fee records** with paid/pending/overdue status
- **10 notifications** across announcements, exam reminders, and homework

---

## Design System

### Colors

| Token | Value | Usage |
|-------|-------|-------|
| `--primary` | `#1a56db` | Buttons, active states, badges |
| `--accent` | `#0ea5e9` | Highlights, charts |
| `--success` | `#10b981` | Present, paid, active badges |
| `--warning` | `#f59e0b` | Pending, late status |
| `--danger` | `#ef4444` | Absent, overdue, delete |
| `--purple` | `#8b5cf6` | Classes, elective subjects |
| `--bg` | `#f8fafc` | Page background |
| `--text-primary` | `#111827` | Main text |

### Typography

- **Display / Branding:** DM Serif Display
- **Body / UI:** DM Sans (weights 300–700)

### Components

- Stat cards with hover lift effect
- White cards with subtle box shadows
- Badge system (success, danger, warning, primary, purple, cyan, gray)
- Progress bars
- CSS donut chart
- Bar chart placeholders with grid overlay
- Activity feed
- Event timeline
- Notification cards with unread indicator

---

## Responsive Behavior

| Breakpoint | Behavior |
|------------|----------|
| > 900px | Fixed sidebar, collapsible to icon-only mode |
| ≤ 900px | Sidebar hidden, slides in as a drawer via hamburger menu |
| ≤ 580px | Stats grid collapses to 2 columns |

---

## Interactivity

All navigation and interactions are handled with vanilla JavaScript:

- **Section switching** — clicking any sidebar item shows the correct page and hides all others
- **Sidebar toggle** — collapses/expands on desktop; opens/closes as overlay drawer on mobile
- **Student profile modal** — clicking the eye icon on any student row opens a detailed profile modal
- **Add Student modal** — form with all required fields, opens via the Add Student button
- **Attendance toggles** — each student has P / A / L buttons; "Mark All" buttons set the entire class at once
- **Table search** — live search filters rows as you type in the search box

---

## Customization

### Changing the School Name

Find the logo text in the sidebar and header:

```html
<div class="logo-text">Edu<span>Core</span></div>
```

Replace `EduCore` with your school's name.

### Adding Real Data

Replace the data arrays at the top of the `<script>` block:

```javascript
const studentData = [ /* your data here */ ];
const teacherData = [ /* your data here */ ];
const feeData     = [ /* your data here */ ];
```

### Changing the Color Scheme

All colors are CSS variables in `:root {}`. Change `--primary` to update the entire theme:

```css
:root {
  --primary: #1a56db;  /* change this to your school color */
}
```

---

## External Dependencies

All loaded via CDN — no npm install needed:

| Library | Version | Purpose |
|---------|---------|---------|
| [Google Fonts](https://fonts.google.com) | — | DM Sans + DM Serif Display |
| [Font Awesome](https://fontawesome.com) | 6.5.0 | All icons throughout the UI |

---

## Browser Support

| Browser | Support |
|---------|---------|
| Chrome 90+ | ✅ Full |
| Firefox 88+ | ✅ Full |
| Edge 90+ | ✅ Full |
| Safari 14+ | ✅ Full |
| IE 11 | ❌ Not supported |

---

## Limitations (Prototype)

Since this is a frontend-only prototype:

- Data is not persisted — refreshing the page resets everything
- Forms do not submit to a real backend
- Charts are static visual placeholders (no real chart library)
- Authentication is purely cosmetic (no real login)
- Search only filters the currently visible table rows

These would all be replaced with real implementations in production.

---

## Roadmap (For Full Development)

When converting this prototype into a production system, consider:

- [ ] Backend API (Node.js / Django / Laravel)
- [ ] Database (PostgreSQL / MySQL)
- [ ] Authentication & role-based access (Admin, Teacher, Parent, Student)
- [ ] Real chart library (Chart.js or Recharts)
- [ ] Email/SMS notification integration
- [ ] PDF report generation
- [ ] Mobile app (React Native / Flutter)
- [ ] Multi-school / multi-branch support

---

## License

This prototype is provided as a UI demonstration. Free to use, modify, and build upon for educational or commercial projects.

---

*Built with HTML, CSS & Vanilla JavaScript — EduCore School Management System Prototype*
