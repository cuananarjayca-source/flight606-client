# ✈️ Flight 606 — Airline Booking System

![Flight-Booking-System](/public/Homepage.png)

> A premium, full-stack web application for flight search, seat selection, passenger management, and booking confirmation — built with the "Flight 606" luxury aviation aesthetic.

---

[![Status](https://img.shields.io/badge/status-active-success.svg)](https://heroic-vacherin-4f50fb.netlify.app)
[![Deployment](https://img.shields.io/badge/deployed%20on-Netlify-00C7B7?logo=netlify)](https://heroic-vacherin-4f50fb.netlify.app)
[![Node.js](https://img.shields.io/badge/backend-Node.js%20%2B%20Express-339933?logo=node.js)](https://nodejs.org)
[![MongoDB](https://img.shields.io/badge/database-MongoDB-47A248?logo=mongodb)](https://www.mongodb.com)
[![Bootstrap](https://img.shields.io/badge/frontend-Bootstrap%205-7952B3?logo=bootstrap)](https://getbootstrap.com)
[![Vue.js](https://img.shields.io/badge/framework-Vue.js%203-4FC08D?logo=vue.js)](https://vuejs.org)
[![Vite](https://img.shields.io/badge/build-Vite-646CFF?logo=vite)](https://vite.dev)
[![Pinia](https://img.shields.io/badge/state-Pinia-F7C948?logo=pinia)](https://pinia.vuejs.org)
[![Figma](https://img.shields.io/badge/design-Figma-F24E1E?logo=figma)](https://www.figma.com/design/kgJUpm3z5jK5Ya3jaDYiQ8/APRIL-PROJECT?node-id=37-6284&t=KInoG9fmcZiqOFzD-0)


---

## 📖 Description

**Flight 606** is a full-stack airline booking web application developed by B606 Group 2 as part of the MCP Project. It provides an end-to-end travel reservation experience — from searching flights and choosing seats to issuing digital boarding passes with QR codes.

The platform is designed around a premium "Flight 606" brand identity: a dark, editorial aesthetic anchored by golden-sand accents that evoke business-class travel.

**Reference Links:**
- 🌐 [Live Demo](https://heroic-vacherin-4f50fb.netlify.app)
- 🎨 [Figma Mockups](https://www.figma.com/design/kgJUpm3z5jK5Ya3jaDYiQ8/APRIL-PROJECT?node-id=37-6284&t=KInoG9fmcZiqOFzD-0)
- 📐 [System Blueprint / ERD](https://drive.google.com/file/d/1k1MKMJo1E8MnAvm5vZh1KCKPLOtEL_ba/view)

---

## ✨ Features

- **Smart Flight Search** — One-way, Round-trip, and Multi-city search with dynamic filtering by price, time, and stops
- **Interactive Seat Selection** — 2D cabin map with real-time seat availability, lock timers, and class indicators
- **Multi-Passenger Booking** — Supports group bookings, companion profiles, and guest checkout (no account required)
- **Digital Boarding Passes** — QR-code-enabled, mobile-friendly boarding pass generated instantly on confirmation
- **Itinerary Management** — Organize multiple bookings under a named travel itinerary
- **Admin Dashboard** — Secure portal for flight CRUD operations, seat management, and passenger manifest export
- **Mock Payment Flow** — Stripe Test Mode simulation (no real transactions)
- **Notification System** — In-app alerts for booking updates and flight status changes
- **Responsive Design** — Fully functional on desktop, tablet, and mobile via Bootstrap 5

---

## 🖥️ Visuals

> Screenshots and GIFs of the live application are linked below. All screens reflect the deployed version at [heroic-vacherin-4f50fb.netlify.app](https://heroic-vacherin-4f50fb.netlify.app).

| Screen | Description |
|:---|:---|
| **Hero / Landing** | Full-bleed aircraft background with frosted-glass search widget and dynamic tagline carousel |
| **Flight Results** | Filterable list of matching flights with price, stops, duration, and airline info |
| **Seat Map** | 2D cabin grid with live availability and session-based seat locking |
| **Booking Confirmation** | PNR code, flight summary, passenger list, and QR-coded boarding pass |
| **Admin Dashboard** | Data-rich table interface for flight and seat management |

> 🎨 For high-fidelity screen designs, see the [Figma prototype](https://www.figma.com/design/kgJUpm3z5jK5Ya3jaDYiQ8/APRIL-PROJECT?node-id=37-6284&t=KInoG9fmcZiqOFzD-0).

---

## ⚙️ Installation

### Requirements

- **Node.js** v18 or higher ([Download](https://nodejs.org))
- **npm** v9+ (bundled with Node.js)
- **MongoDB** — local instance or [MongoDB Atlas](https://www.mongodb.com/atlas) cloud cluster
- A modern browser: Chrome, Firefox, Safari, or Edge

---

### Steps

**1. Clone the repository**

```bash
git clone https://github.com/<your-org>/flight-606.git
cd flight-606
```

**2. Install dependencies**

```bash
npm install
```

**3. Configure environment variables**

Create a `.env` file in the project root:

```env
PORT=3000
MONGODB_URI=mongodb://localhost:27017/flight606
JWT_SECRET=your_jwt_secret_here
NODE_ENV=development
```

> For production, replace `MONGODB_URI` with your MongoDB Atlas connection string.

**4. Seed the database** *(optional — loads sample flights and airports)*

```bash
npm run seed
```

**5. Start the development server**

```bash
npm run dev
```

**6. Open the app**

Visit [http://localhost:3000](http://localhost:3000) in your browser.

---

## 🚀 Usage

### Booking a Flight

1. On the landing page, enter your **origin**, **destination**, and **travel date** in the search widget
2. Select a trip type: **One Way**, **Round Trip**, or **Multi-city**
3. Click **"Book now!"** to view available flights
4. Choose a flight from the results and select your **seat** from the cabin map
5. Fill in **passenger details** (name, passport, contact info)
6. Complete the **mock payment** (use any test card number)
7. Receive your **Booking Confirmation** with PNR and digital boarding pass

### Admin Access

Navigate to `/login?redirect=/admin-dashboard` and sign in with admin credentials to access the management portal.

```
Default Admin Credentials (development only):
  Email:    admin@flight606.com
  Password: admin123
```

> ⚠️ Change these credentials before any public-facing deployment.

---

## 🆘 Support

For issues or questions:

- **GitHub Issues:** [Open an issue](https://github.com/cuananarjayca-source/flight606-client)
- **Email:** cuananarjay.ac@gmail.com
- **Trello Board:** TBD (link to be added)

Please include your browser, OS, and a description of the problem when reporting bugs.

---

## 🗺️ Roadmap

### v1.x (Current — In Progress)
- [x] Flight search (One-way, Round-trip, Multi-city)
- [x] Seat selection with lock timer
- [x] Passenger details and booking flow
- [x] Mock payment processing
- [x] Digital boarding pass with QR code
- [x] Admin dashboard (flight + seat management)
- [x] User dashboard and trip history
- [x] Notifications system
- [ ] Itinerary management (in progress)

### v2.0 (Planned)
- [ ] Live Browser Geolocation API integration
- [ ] Real-time pricing sync from flight database
- [ ] Loyalty / reward points system
- [ ] OAuth social login (Google, Facebook)
- [ ] Email notifications (SendGrid integration)

### v3.0 (Stretch Goals)
- [ ] GDS / third-party airline API integration
- [ ] Multi-language support (i18n)
- [ ] Accessibility (WCAG 2.1 AA compliance)
- [ ] Progressive Web App (PWA) offline support

---

## 🤝 Contributing

Contributions from team members are welcome! Here's how to get started:

**1. Fork and clone the repo**

```bash
git clone https://github.com/cuananarjayca-source/flight606-client.git
```

**2. Create a feature branch**

```bash
git checkout -b main
```

**3. Make your changes and commit**

```bash
git commit -m "feat: add your feature description"
```

Follow [Conventional Commits](https://www.conventionalcommits.org/) for commit messages (`feat:`, `fix:`, `docs:`, `chore:`).

**4. Push and open a Pull Request**

```bash
git push origin feature/your-feature-name
```

Open a PR against the `main` branch with a clear description of the changes.

### Code Standards

- Run lint before pushing:
  ```bash
  npm run lint
  ```
- Run tests:
  ```bash
  npm test
  ```
- All API routes must return structured JSON (success and error cases)
- New features must not break existing Bootstrap 5 responsive layouts

### What We Accept

- Bug fixes with clear reproduction steps
- UI improvements that align with the Flight 606 design system
- New features discussed and approved in the project Trello board
- Performance improvements backed by measurable data

---

## 👥 Authors & Acknowledgments

**B606 – Group 2 MCP Project**

| Role | Contributor |
|:---|:---|
| Project Lead | Rojan Pilar |
| Frontend Design | Arjay Cuanan, Rojan Pilar, Nathaniel Medina |
| Backend Development | Maiki Raval |
| Database Design | Nathaniel Medina |
| QA / API Testing | Arjay Cuanan, Maiki Raval |
| Technical Specification Design | Arjay Cuanan, Nathaniel Medina, Maiki Raval | 

Special thanks to:
- **Bootstrap** — for the responsive grid foundation
- **Vue.js** - for structured SPA Web
- **MongoDB** — for the flexible document model that made nested booking data elegant
- **Figma** — for the design system collaboration tools
- **Netlify** — for frictionless frontend deployment

---


Copyright (c) 2026 B606 Group 2 MCP Project

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software to use, copy, modify, merge, publish, distribute, sublicense,
and/or sell copies of the Software, subject to the standard MIT conditions.
```

---

## 📌 Project Status - In progress

**🟢 Active Development** — The project is currently in its final integration phase ahead of the academic demo. Core features are deployed and functional at the live link below.

> 🌐 **Live Demo:** [heroic-vacherin-4f50fb.netlify.app](https://heroic-vacherin-4f50fb.netlify.app)
>
> 📋 **TSD:** See [`Technical_Specification_Documentation.md`](./Technical_Specification_Documentation.md) for the full architecture and feature specification.

---

*Made with ☕ and ✈️ by B606 Group 2*
