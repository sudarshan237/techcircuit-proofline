# Proofline — TechCircuit Hackathon Build

A browser-local MVP prototype for pre-publication brand governance.

## Run it
Open `index.html` in a modern browser. No build step, package manager, server, environment variables, or API key is required.

## Implemented in this prototype
- Deterministic checks for unsupported superlatives and absolute claims, preferred terminology, off-brand terms, urgency language, all-caps tone, long sentences, and non-descriptive link text.
- Finding details with severity, explanation, sample policy/source reference, detected excerpt, and suggested action.
- Applying simple replacement suggestions or marking findings reviewed.
- Editing local glossary terms and approved facts. An exact match is not independent fact verification.
- Review note and local approval decision; high-severity open findings block approval.
- Import of UTF-8 plain text, Markdown, CSV, or HTML as plain text; review export to JSON.
- Browser `localStorage` for current state and local activity log.

## Material limitations
- No external AI/LLM API. The rule engine uses deterministic string/regular-expression heuristics and is not a compliance or legal determination.
- No server/database, accounts, enforceable multi-user role-based access, central audit log, or multi-device data sharing.
- No image analysis/OCR, PDF/DOCX extraction, visual asset checking, or live integrations.
- Do not enter confidential brand materials. Default facts and policies are sample data and must be replaced by verified brand rules.

## Stack and architecture
Single-page HTML, CSS and vanilla JavaScript. Text checks run in the browser; state and activity are stored in `localStorage`; reports are exported client-side as JSON. No external dependencies.

## Suggested production hardening
Add identity and tenant isolation, server-side data storage, versioned approved-source records, permissions enforced by the backend, traceable evidence, secure audit logging, evaluation data, and model/API governance before using real company content.
