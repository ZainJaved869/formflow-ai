# FormFlow AI – AI‑Powered Form Builder SaaS

**FormFlow AI** is a complete, production‑ready SaaS application that allows users to build intelligent forms using AI, collect responses, and gain insights. It comes with a drag‑and‑drop builder, AI‑generated fields, analytics, and a beautiful glassmorphism UI with dark/light mode.

## Features
- AI Form Generator (Google Gemini)
- Drag‑and‑drop builder (11 field types)
- Public forms with shareable links
- Submissions with CSV/Excel/PDF export
- Analytics dashboard (stats + charts)
- QR code generator
- Email & WhatsApp notifications
- Form templates (6 pre‑built)
- Webhooks & REST API
- Multi‑tenant teams
- Admin panel with user management
- Subscription plans (Free/Pro/Business) – Stripe‑ready
- Fully responsive glassmorphism design

## Requirements
- PHP 8.2+
- MySQL 8.0+
- Composer
- Node.js (optional for frontend assets)

## Installation
1. Upload all files to your server (or extract the zip).
2. Run `composer install` (if vendor folder is not included).
3. Copy `.env.example` to `.env` and update credentials:
   - Database (DB_*)
   - Mail (MAIL_*)
   - Gemini API key (GEMINI_API_KEY)
   - Optional: Stripe (STRIPE_*), Twilio (TWILIO_*)
4. Run `php artisan key:generate`.
5. Run `php artisan migrate --seed` (this creates tables and seeds templates/plans).
6. Run `php artisan storage:link`.
7. Configure your web server (Apache/Nginx) to point to the `public/` folder.
8. (Optional) Run `npm install && npm run build` for frontend assets if using Vite.

## Default Admin User
- No default admin user is created. You can create one via `php artisan tinker` or register normally and set `is_admin = 1` in the database.

## Documentation
Full documentation is available in the `Documentation/` folder.

## Support
For support, contact: support@yourdomain.com