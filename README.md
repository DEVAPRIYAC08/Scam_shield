# InvestorShield

InvestorShield is a safety-first, demo-ready Next.js app for explaining suspicious financial messages. It does not provide investment recommendations, price predictions, trading signals, or fraud determinations.

## Run locally

```bash
npm install
npm run dev
npm run build
npm run start
```

Open `http://localhost:3000`.

## Demo mode

With empty `AI_API_KEY`, `AI_PROVIDER`, and `OCR_PROVIDER` values (see `.env.example`), analysis uses local deterministic rules. This detects financial risk patterns, extracts claims, explains absent evidence, and explicitly reports that independent verification is unavailable. Screenshot upload includes a browser preview plus an editable manual-text fallback; no image is permanently stored.

## Architecture

- `app/api/analyze`: structured analysis API
- `lib/analyzer.ts`: deterministic analysis engine
- `lib/ai/analyze.ts`: future AI-provider abstraction
- `app/api/ocr`: OCR-provider placeholder with transparent demo response
- `components`: responsive UI, preferences, form, results

## Privacy and safety

Do not enter passwords, OTPs, PINs, account credentials, or CVV. Browser history is local only. The app can identify patterns but cannot confirm whether an organization or offer is genuine; official verification is not simulated in demo mode.

## Deploy

Deploy to any Next.js-compatible host. Add provider variables only when implementing a real AI/OCR provider behind the included abstractions.
