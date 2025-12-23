# GrubToGo 🍔

GrubToGo is a food ordering web application built using React and Vite. The platform supports role-based access for Students and Caterers, allowing users to browse food deals, view limited-time discounts, and interact with store offerings.

## Tech Stack
- React
- Vite
- JavaScript
- HTML / CSS

## Key Features

### Authentication & User Roles
- Users can register as **Student** or **Caterer** using a role toggle.
- Student emails must end with `@pace.edu`.
- Caterer emails must end with `.staff@pace.edu`.
- After successful registration:
  - Students are redirected to the Student dashboard.
  - Caterers are redirected to the Caterer dashboard.

### Deals Page (Limited-Time Discounts)
- Displays promotional food items from multiple stores.
- Each deal includes:
  - Original price
  - Discount percentage
  - Automatically calculated discounted price
  - Live countdown timer until expiration
- When a deal expires, the UI visually disables the item and interaction.

### Frontend Deal Logic
- Deal data is seeded from a local data file and enriched with store metadata.
- Discounted prices and countdown timers are derived dynamically on the frontend.
- Vite hot reload allows instant UI updates during development.

### Caterer Workflow (Current Implementation)
- Caterers can update or add deals by modifying the local deals data file.
- Supports editing item details, pricing, discounts, and expiration times.
- Designed to be easily extended to backend storage such as Firebase / Firestore.

## Project Structure
- `src/pages/Register/` – User registration and role selection
- `src/pages/Deals/` – Deals page UI and logic
- `src/assets/` – Static data and helper functions

## Team Contribution
This project was developed as a **team-based software engineering project**.  
My primary responsibility was **frontend development**, including UI components, page layouts, state management, and implementation of core features such as role-based navigation and the deals page. I also collaborated with the team on feature planning and design decisions.

## Future Enhancements
- Replace static deal data with Firestore collections
- Enable real-time updates for deals
- Add checkout and order history functionality
- Provide analytics dashboards for caterers

## Run Locally
```bash
npm install
npm run dev
