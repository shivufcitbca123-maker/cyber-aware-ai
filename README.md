# CyberAware Pro

**Think Before You Click. Pause. Verify. Protect.**

CyberAware Pro is a local-first cybersecurity awareness mini-project for college students. It teaches practical habits with fictional examples and interactive exercises. It does not perform scans, send messages, collect credentials, or connect to a live AI service.

## Requirements

- Node.js 20.19+ or 22.12+ (Node.js 24 also works)
- npm, included with Node.js
- VS Code or another editor

## Run locally

Open this project folder in VS Code, then run these commands in the integrated terminal:

```powershell
npm.cmd install
npm.cmd run dev
```

Open the local URL printed by Vite (usually `http://localhost:5173`). To create and check a production build:

```powershell
npm.cmd test
npm.cmd run build
```

`npm.cmd` is used in PowerShell because some Windows execution policies block the `npm.ps1` shim.

## Demo account

- **Email:** `demo@cyberaware.local`
- **Password:** `CyberAware@123`

On the Login page, choose **Use Demo Account**, then choose **Sign in**. The demo account is for this educational application only. The client-side session flag is not production authentication. Passwords are not stored in browser storage or transmitted.

## What is included

- Responsive home page and navigation for learning, phishing practice, quiz, checklist, awareness kit, FAQ, login, dashboard, and project sources.
- Plain-language lessons about phishing, passwords, scams, and device protection.
- Fictional phishing spotter examples and a knowledge quiz with feedback and review.
- Local checklist, activity summary, and lesson completion progress stored in browser local storage.
- A local rule-based FAQ helper with predefined guidance and an unknown-question fallback. It is not a live AI model and does not store questions.
- A CSS poster that can be printed, plus a copyable/downloadable campaign message.
- Protected client-side demo dashboard and logout.
- Keyboard-operable controls, focus styles, reduced-motion support, and responsive mobile navigation.

## Privacy and safety notes

This is an educational demo, not a real authentication service, professional incident response service, or security audit. The dashboard requires only a session flag in `sessionStorage`; entered passwords are never saved. Checklist and learning activity are optional local demo data in `localStorage` and can be cleared in browser settings. The app does not use analytics, external AI APIs, or third-party data collection.

The lessons and sample messages are fictional and defensive. Use official support channels for real security incidents. Trusted links are listed on the **About / Sources** page and open in a new tab.

## Project structure

```text
src/
  data/
    content.ts          # Lesson, checklist, quiz, spotter, and resource data
  lib/
    auth.ts             # Replaceable client-side demo authentication abstraction
    progress.ts         # Typed, local-only progress storage
  pages/
    Pages.tsx           # Route page components and interactions
    Pages.test.tsx      # Login and demo-authentication tests
  App.tsx               # Navigation, routes, and protected dashboard
  main.tsx              # React entry point
  styles.css            # Responsive theme, components, and print styling
  testSetup.ts          # Vitest matchers
index.html
vite.config.ts
tsconfig.json
tsconfig.app.json
package.json
PROJECT_REPORT.md
TESTING_CHECKLIST.md
```
