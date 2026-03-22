# SDR Pages - AI SDR Prospect Intel Pages

**URL:** https://sdr.42agency.com
**Hosting:** Vercel (project: `sdr-pages`)
**Deploy:** Auto-deploys on git push to main

---

## Purpose

Personalized intel pages for AI SDR outbound campaigns. Each page is created for a specific prospect/company and linked in outreach emails.

**These pages are ephemeral** - they typically live 30-90 days during an outbound campaign.

---

## Structure

```
sdr-pages/
├── [company-slug]/
│   └── index.html
├── vercel.json
└── CLAUDE.md
```

**Naming convention:** `company-hexcode` (e.g., `flexor-030d27`, `luminai-9cf0ae`)

The hex code ensures unique URLs and prevents conflicts.

---

## Creating New Pages

### Via AI SDR Agent

The AI SDR agent automatically:
1. Creates the page in this repo
2. Commits and pushes
3. Vercel auto-deploys

### Manual

```bash
cd ~/sdr-pages

# Create page directory
mkdir mycompany-abc123
# Add index.html with intel content

# Commit and push
git add . && git commit -m "Add mycompany-abc123" && git push
```

---

## Design System

Use the same Intel design system as intel.42agency.com:

- **Accent:** `#DFFE68` (lime yellow)
- **Text:** `#1a1a1a` (near-black)
- **Borders:** 2px solid black
- **Shadows:** `4px 4px 0px 0px #1a1a1a`
- **Font:** Inter

See `/Users/42agency/.claude/CLAUDE.md` for full design system.

---

## Shared Assets

Reference shared assets from intel.42agency.com:
- Logo: `https://intel.42agency.com/42-logo.png`
- Fonts: Google Fonts (Inter)

---

## Page Lifecycle

| Stage | Duration | Action |
|-------|----------|--------|
| Active | 0-30 days | Linked in outbound emails |
| Stale | 30-90 days | May still get visits |
| Archive | 90+ days | Can be deleted |

**No manifest needed** - pages can be freely created/deleted without coordination.

---

## Analytics

Each page should include:
- GTM: `GTM-MM5BTNS`
- HubSpot tracking (portal: `44888286`)

---

## Related

- **intel.42agency.com** - Lead magnets, tools, playbooks (permanent content)
- **AI SDR Agent** - `~/.claude/agents/ai-sdr.md`
