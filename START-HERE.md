# Start Here

Welcome to ClickCampaigns God Mode! Follow these steps to get your AI marketing team up and running.

---

## Step 1: Open This Folder

Open this entire folder in **Cursor** or **VS Code**.

- In Cursor: **File → Open Folder** → select this folder
- In VS Code: **File → Open Folder** → select this folder

---

## Step 2: Launch Claude Code

Open the terminal inside your editor and paste this prompt.

**If the MCP is already connected:**

```
Read the CLAUDE.md file, use the ClickCampaigns MCP, and start my campaign.
```

**If the MCP is NOT connected yet (just paste your token right in):**

```
Read the CLAUDE.md file, use the ClickCampaigns MCP, and start my campaign with this token: cc-paste-your-token-here
```

Replace `cc-paste-your-token-here` with the token from Step 7 of the Campaign Wizard.

That's it! Alex will introduce himself and your team of 22 marketing specialists.

---

## Step 3: Set Up API Keys (Optional but Recommended)

For the best results (AI images, stock photos), add API keys:

1. Find the file called `.env.example` in this folder
2. Make a copy of it and rename the copy to `.env`
3. Open `.env` and paste your API keys:

| Key | What It Does | Where to Get It |
|-----|-------------|-----------------|
| GEMINI_API_KEY | AI-generated images for your marketing assets | [ai.google.dev](https://ai.google.dev/) (free) |
| PEXELS_API_KEY | Stock photos for landing pages and PDFs | [pexels.com/api](https://www.pexels.com/api/) (free) |
| FIRECRAWL_API_KEY | Clone any webpage as a starting point | [firecrawl.dev](https://www.firecrawl.dev/) |

Everything works without these keys — they just make your assets look better.

Your `.env` file is already protected by `.gitignore`, so your keys will never be uploaded to GitHub.

---

## What Can You Ask Alex?

Here are some example requests to get you started:

- "Build me a VSL hybrid funnel with a sales page, checkout page, and upsell page for my online course."
- "Create a webinar registration page with countdown timer and 3 bullet points on what they'll learn."
- "Write a 7-email launch sequence for my product launch. Include cart open, social proof, and urgency emails."
- "Create Facebook ad copy with 5 headline variations targeting small business owners."
- "Write a 20-page PDF guide called '10 Steps to Double Your Revenue' with checklists in each chapter."

---

## Need Help?

- [God Mode Guide](https://clickcampaigns.ai/god-mode-guide) — Full setup and usage guide
- [Settings](https://clickcampaigns.ai/settings?tab=god-mode) — Manage tokens and settings
- [Support](https://support.groovedigital.com/) — Get help from the team
