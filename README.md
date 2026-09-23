# NOVA — Real-World Indian Marketplace

Portfolio-ready full-stack e-commerce project built with React + Vite, Express and SQLite.

## Highlights
- 168 curated products across 14 departments
- Local deterministic SVG product artwork — no broken external product-photo URLs
- Indian-first INR pricing with realistic category ranges
- Working search, categories, subcategories, sorting
- Favorites and cart persistence
- Product details with ratings and community comments
- Add-a-review flow for signed-in users
- Email OTP auth with development OTP fallback
- Password auth with bcrypt + JWT
- Checkout, orders and delivery tracking UI
- Responsive premium light theme with subtle motion

## Run
### Backend
```powershell
cd server
npm install
npm run seed
npm run dev
```
Runs on http://localhost:5000

### Frontend
```powershell
cd client
npm install
npm run dev
```
Open the Vite URL, usually http://localhost:5173 or http://localhost:5174.

## Demo
Email: demo@nova.store
Password: Nova@123

For real email OTP, configure SMTP values in `server/.env` using `.env.example`.


### Media architecture
Product and reviewer artwork is generated locally during `npm run seed` and served by Express under `/media`. The frontend prefixes local media URLs with the API server origin, so images work correctly when Vite runs on either port 5173 or 5174.

The seed creates 168 products (12 per department), 840 seeded reviews, reviewer avatars, and a local fallback image.
