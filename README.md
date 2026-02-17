# governr Trust & Security Website

A static website showcasing governr's commitment to security, privacy, and responsible AI governance.

## Overview

This is the Trust & Security page for [governr.ai](https://governr.ai), an AI governance platform. The page highlights:

- **Security & Data Protection** - Enterprise-grade encryption and access controls
- **Privacy & Compliance** - GDPR compliant data handling
- **AI Ethics & Responsible AI** - Bias detection and model transparency
- **Service Reliability** - 99.9% uptime SLA
- **Certifications & Audits** - Working towards SOC 2, ISO 27001
- **Data Governance** - Clear retention and deletion policies

## Project Structure

```
trust-governr-website/
├── public/
│   ├── index.html          # Main HTML page
│   ├── styles.css          # Stylesheet
│   ├── 404.html            # 404 error page
│   ├── llms.txt            # LLM-readable documentation
│   └── images/
│       ├── governr logo black.svg
│       ├── governr logo blue.svg
│       └── governr logo white.svg
├── firebase.json           # Firebase configuration
├── .firebaserc             # Firebase project settings
├── .gitignore              # Git ignore rules
└── README.md               # This file
```

## Prerequisites

- [Node.js](https://nodejs.org/) (v18 or higher recommended) - for running local servers
- [Firebase CLI](https://firebase.google.com/docs/cli) - for deployment

## Running Locally

### Option 1: Using npx serve (Recommended)

```bash
npx serve public
```

The site will be available at `http://localhost:3000`

### Option 2: Using Python's built-in server

If you have Python installed:

```bash
# Python 3
python -m http.server 8000 -d public

# Python 2
python -m SimpleHTTPServer 8000 -d public
```

The site will be available at `http://localhost:8000`

### Option 3: Using Live Server (VS Code)

1. Install the [Live Server extension](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
2. Right-click on `public/index.html`
3. Select "Open with Live Server"

## Deploying on Firebase

### Initial Setup

1. **Install Firebase CLI** (if not already installed):
   ```bash
   npm install -g firebase-tools
   ```

2. **Login to Firebase**:
   ```bash
   firebase login
   ```

3. **Verify the project configuration** (optional):
   ```bash
   firebase use --add
   ```
   Select `governr-ai` when prompted.

### Deployment

To deploy the website to Firebase Hosting:

```bash
# Deploy to the trust target
firebase deploy --only hosting:trust
```

Or simply:

```bash
firebase deploy
```

The site is configured to deploy to the `trust-governr` hosting channel in the `governr-ai` Firebase project.

### Preview Before Deploying

To preview your changes before deploying:

```bash
firebase emulators:start --only hosting
```

This will start a local emulator at `http://localhost:5000`

## Firebase Configuration

The project uses the following Firebase configuration:

- **Project ID**: `governr-ai`
- **Hosting Target**: `trust`
- **Public Directory**: `public`
- **Live URL**: https://trust.governr.ai

## Technologies Used

- HTML5
- CSS3 (with CSS Grid and Flexbox)
- Vanilla JavaScript
- Google Fonts (JetBrains Mono, Space Grotesk)
- Firebase Hosting

## Contact

For questions or concerns about security and privacy:

- **Email**: [info@governr.ai](mailto:info@governr.ai)
- **Address**: governr AI, 41 Luke St, London EC2A 4DP
- **LinkedIn**: [linkedin.com/company/governr](https://www.linkedin.com/company/governr)

## License

© 2026 governr.ai. All rights reserved.