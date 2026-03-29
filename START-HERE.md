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

## Step 3: Get Your Auth Token

You need an auth token to connect to ClickCampaigns. This is a one-time setup.

1. Go to **[clickcampaigns.ai/cli-auth](https://clickcampaigns.ai/cli-auth)** (you'll need to log in)
2. Click **"Generate CLI Token"**
3. Copy the token (starts with `cliauth-`) — you'll only see it once!

> **What is this?** Your auth token connects your AI editor to your ClickCampaigns account. It lets you access all 22 marketing specialists, 73 skill files, and the full campaign catalog. It's like a password — keep it private.

---

## Step 4: Connect to ClickCampaigns (MCP)

Now connect your editor to ClickCampaigns using the token you just copied.

**Option A — One command in your terminal (easiest, recommended):**

Open your terminal and run this command (replace the token with yours from Step 3):

```bash
claude mcp add clickcampaigns --transport http --url "https://clickcampaigns.ai/mcp" --header "Authorization: Bearer cliauth-PASTE-YOUR-TOKEN-HERE"
```

This writes the config to the correct location automatically. No file editing needed.

**Option B — Add the config file manually:**

Create a file called `.mcp.json` in this project folder (the same folder as this START-HERE.md):

```json
{
  "mcpServers": {
    "clickcampaigns": {
      "type": "url",
      "url": "https://clickcampaigns.ai/mcp",
      "headers": {
        "Authorization": "Bearer cliauth-PASTE-YOUR-TOKEN-HERE"
      }
    }
  }
}
```

> **For Cursor:** Go to **Settings → MCP** and paste the config there instead.

**After connecting (both options):** Start a new Claude Code session (MCP servers only load at session start), then say:

```
Read the CLAUDE.md file, use the ClickCampaigns MCP, and introduce yourself as Alex.
```

---

## Step 5: Start Building

Alex will introduce himself and your team of 22 marketing specialists. You're ready to go!

You can start working right away — browse the catalog, explore skills, or ask Alex for recommendations. No campaign needed to get started.

---

## Step 6: Load a Campaign (Optional)

If you've created a campaign in the ClickCampaigns Campaign Wizard, you can load it for full context:

1. Go to your campaign workspace at **[clickcampaigns.ai](https://clickcampaigns.ai)**
2. Create a campaign using the **7-step Campaign Wizard**
3. On **Step 7**, copy your campaign token (starts with `cc-`)
4. Tell Alex: **"Load my campaign with token cc-paste-your-token-here"**

Alex will load your brand kit, selected work items, execution plan, and specialist assignments. This gives him everything he needs to create production-ready marketing assets for your specific campaign.

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
