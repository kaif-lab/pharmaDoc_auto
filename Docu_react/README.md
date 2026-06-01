# DocuPharma AI — React + Node.js

Full-stack pharma regulatory document automation.
React 18 · Vite · Zustand · React Router · Node.js · Express · Anthropic Claude

## Quick Start

### Backend
cd docupharma-server && npm install
# Add ANTHROPIC_API_KEY to .env
npm run dev   # http://localhost:3001

### Frontend
cd docupharma-react && npm install
npm run dev   # http://localhost:5173

## Pages
  /            Landing page
  /dashboard   Analytics & pipeline overview
  /app         All 6 AI modules
  /settings    API key, compliance, team, billing

## 6 AI Modules
  Draft Generation     POST /api/modules/draft
  Gap Analysis         POST /api/modules/gap
  Safety Narratives    POST /api/modules/safety
  Cross-Reference      POST /api/modules/xref
  Localisation         POST /api/modules/locale
  Benefit-Risk         POST /api/modules/br

Add ?stream=true to any module for SSE streaming.

## Tech Stack
  Frontend: React 18, Vite, Zustand, React Router, Axios
  Backend:  Express 4, @anthropic-ai/sdk, Helmet, Morgan
  Model:    claude-sonnet-4-20250514
