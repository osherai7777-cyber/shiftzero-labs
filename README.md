# CISO as a Service — Landing Page

A professional landing page for fractional CISO services, targeting startups and small companies.

**Live:** https://<username>.github.io/ciso-as-a-service/

## What's on the page

- **Hero** — bold positioning statement, CTA, "CISO at the Technion" credential
- **Services** — compliance frameworks (NIST, FedRAMP, HIPAA, HITRUST, SOC 2, ISO 27001, GDPR) + risk assessment, security program & policy, architecture review, incident response, security awareness & training
- **Approach** — 4-step process (understand → roadmap → execute → stay engaged)
- **About** — CISO at the Technion background, credentials
- **Contact form** — Formspree-powered free form (replaces `YOUR_FORMSPREE_ID` in index.html)

## Design

- Dark navy/charcoal theme with teal accent (#5eead4)
- Inter font (Google Fonts)
- Responsive: works on mobile, tablet, desktop
- Pure HTML + CSS — no JavaScript dependencies, no build step

## Form setup (free)

The contact form uses [Formspree](https://formspree.io/) (free tier: 50 submissions/month).

1. Go to https://formspree.io/ and create a free account
2. Create a new form — you'll get a form ID like `xxxxxxxxxxxxx`
3. Replace `YOUR_FORMSPREE_ID` in `index.html` line with your form ID:
   ```
   action="https://formspree.io/f/YOUR_FORMSPREE_ID"
   ```
4. Form submissions will be emailed to the email you verified with Formspree

No backend, no server, no cost.

## Deploy

GitHub Pages serves this automatically from the `main` branch (or `master`).

### Option A: Using gh CLI

```bash
# Create the repo (replace with your GitHub username)
gh repo create <username>/ciso-as-a-service --public --description "Fractional CISO landing page"

# Push files
git remote add origin git@github.com:<username>/ciso-as-a-service.git
git add index.html README.md
git commit -m "Initial landing page"
git push -u origin main
```

### Option B: Manual

1. Create a new public repository on GitHub: `ciso-as-a-service`
2. Upload `index.html` and `README.md`
3. Go to Settings → Pages → Source: main branch → Save
4. Site live at `https://<username>.github.io/ciso-as-a-service/`

## Customization

- **Formspree ID** — replace `YOUR_FORMSPREE_ID` in `index.html`
- **Colors** — edit the CSS `:root` variables at the top of the embedded `<style>` block
- **Services** — edit the `services-grid` section
- **About / credentials** — edit the `about` section

## Tech stack

- Single HTML file with embedded CSS
- No JavaScript frameworks
- No build tools
- Google Fonts (Inter)
- Formspree for form handling (free tier)

