# Start Here

Welcome to ClickCampaigns God Mode! Follow these steps to get your AI marketing team up and running.

---

## Step 1: Make It Your Own

After cloning, this folder is still linked to the ClickCampaigns template repo. You need to disconnect it and make it your own so your work stays private.

**In GitHub Desktop (easiest):**

1. Open GitHub Desktop
2. Go to **Repository → Repository Settings**
3. Under **Remote**, click **Remove** to disconnect from the template
4. Now go to **Repository → Push** or **Publish Repository** — GitHub Desktop will ask you to create a **new repository** under your own GitHub account
5. Name it whatever you want (e.g., `my-marketing-campaigns`) and choose **Private**

**Or in the terminal:**

```bash
git remote remove origin
```

Then later, create your own repo on GitHub and add it:

```bash
git remote add origin https://github.com/YOUR-USERNAME/your-repo-name.git
git push -u origin main
```

---

## Step 2: Open This Folder in Your Editor

Open this entire folder in **Cursor** or **VS Code**.

- In Cursor: **File → Open Folder** → select this folder
- In VS Code: **File → Open Folder** → select this folder

---

## Step 3: Connect to ClickCampaigns (MCP)

You need a campaign token (`cc-...`) from ClickCampaigns.ai. Get one by creating a campaign — the token is generated on Step 7 of the Campaign Wizard.

**Option A — Let Claude Code do it for you (easiest):**

Open the terminal in your editor and paste this prompt:

```
Add a global MCP server called "clickcampaigns" with type "url", url "https://clickcampaigns.ai/mcp", and an Authorization header set to "Bearer cc-PASTE-YOUR-TOKEN-HERE". Then read the CLAUDE.md file, call get_campaign, and introduce yourself as Alex.
```

Replace `cc-PASTE-YOUR-TOKEN-HERE` with your token. Claude Code will install the MCP and start your campaign.

**Option B — Add the MCP config manually:**

Add this to your Claude Code settings (`~/.claude/settings.json`) or Cursor MCP settings:

```json
{
  "mcpServers": {
    "clickcampaigns": {
      "type": "url",
      "url": "https://clickcampaigns.ai/mcp",
      "headers": {
        "Authorization": "Bearer cc-PASTE-YOUR-TOKEN-HERE"
      }
    }
  }
}
```

Then launch Claude Code and say:

```
Read the CLAUDE.md file, use the ClickCampaigns MCP, and start my campaign.
```

---

## Step 4: Start Building

Alex will introduce himself and your team of 22 marketing specialists. You're ready to go!

---

## Step 5: Set Up API Keys (Optional but Recommended)

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
