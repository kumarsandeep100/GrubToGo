# GrubToGo 🍔

GrubToGo is a food ordering web application built using React and Vite. The platform supports role-based access for Students and Caterers, allowing users to browse deals, place orders, and manage limited-time discounts.

## Tech Stack
- React
- Vite
- JavaScript
- HTML / CSS

## Key Features

### Authentication & Roles
- Users can register as **Student** or **Caterer** using a toggle.
- Student emails must end with `@pace.edu`.
- Caterer emails must end with `.staff@pace.edu`.
- After registration:
  - Students are redirected to the Student dashboard.
  - Caterers are redirected to the Caterer dashboard.

### Deals Page (Limited-Time Discounts)
- Aggregates promotional items from all stores.
- Each deal includes:
  - Original price
  - Discount percentage
  - Automatically calculated discounted price
  - Live countdown timer until expiry
- When a deal expires, the UI visually disables the item.

### Frontend Deal Logic
- Deals are defined in a local data file and enriched with store metadata.
- The UI dynamically derives discounted prices and countdown timers.
- Hot reload allows instant updates during development.

### Caterer Workflow (Current Implementation)
- Caterers can update deals by modifying the local deals data file.
- Supports changing item details, pricing, discounts, and expiration times.
- Designed to be easily extended to backend storage (e.g., Firebase / Firestore).

## Project Structure
- `src/pages/Deals/` – Deals page UI and logic
- `src/assets/` – Static data and helpers
- `src/pages/Register/` – Registration and role selection

## Future Enhancements
- Replace static deal data with a Firestore collection
- Enable real-time updates for deals
- Add order history and checkout flow
- Admin analytics for caterers

## Run Locally
```bash
npm install
npm run dev
