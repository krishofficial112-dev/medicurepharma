# Medicure Pharma | Medical Equipment & Billing

A React + TypeScript + Vite company website for Medicure Pharma, with a built-in local-first billing application.

## Website sections
- Company landing page and responsive navigation
- Medical equipment catalogue and product categories
- About, service and contact sections
- Contact/enquiry UI (demo only; no email/backend integration)
- E-Billing portal entry point into the included billing workspace

## Billing workspace
- Dashboard, point of sale, inventory, quotations, local data/backup, and admin/user management screens
- Local browser storage (IndexedDB) with per-browser local accounts/workspaces
- GST calculations and stock management features included in the application

> **Local-only data warning:** This is not centralized authentication or cloud database storage. Accounts and business data remain in the browser/device where they were created. They do not sync between devices. Regularly export backups and test the application before using it for real transactions. Clearing browser storage can remove data. The first-time setup creates a local admin for that browser profile; this is not a secure public server-side admin system.

## Requirements
- Node.js LTS (18+ recommended)
- npm

## Run locally
1. Download and extract the ZIP or clone this repository.
2. Open a terminal in the project root (the folder containing `package.json`).
3. Install packages:
   ```bash
   npm install
   ```
4. Start the development server:
   ```bash
   npm run dev
   ```
5. Open the URL printed by Vite (usually `http://localhost:5173`).

## Build
```bash
npm install
npm run build
```
The static site is generated in `dist/`. To test the production build locally:
```bash
npm run preview
```

## Deploy from GitHub to Netlify (recommended)
1. Create a new GitHub repository.
2. Upload/push **all files and folders in this project** to the repository root. Ensure `package.json`, `index.html`, `src/`, and `netlify.toml` are at the root, not nested in an extra directory.
3. In Netlify, choose **Add new site → Import an existing project** and connect the GitHub repository.
4. Configure:
   - **Build command:** `npm run build`
   - **Publish directory:** `dist`
   - **Base directory:** leave blank
5. Deploy. The included `netlify.toml` already defines these settings and the SPA redirect.

### Git commands (optional)
From this project folder:
```bash
git init
git add .
git commit -m "Build Medicure Pharma company website and billing app"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```
Replace the remote URL with your repository's actual URL. If GitHub asks you to authenticate, use its supported sign-in/token flow.

## Deploy on Vercel (alternative)
Import the GitHub repository into Vercel and use `npm run build` as the build command and `dist` as the output directory. No environment variables are required for this static/local-first project.

## Before publishing
- Replace illustrative company contact/address details with verified details.
- The contact/enquiry form is not connected to an email service or backend.
- Review product descriptions and prices, if any, before using them commercially.
- Verify invoice formats and tax compliance with your accountant.
- Do not use local-only account setup as a secure shared admin system for a public multi-user business.

## Project structure
```text
.
├── index.html
├── package.json
├── netlify.toml
├── vite.config.ts
├── tsconfig*.json
└── src/
    ├── App.tsx
    ├── CompanyHome.tsx
    ├── company.css
    ├── styles.css
    ├── components/
    ├── pages/
    ├── lib/
    └── types.ts
```
