# Pareas Trello Power-Up — Step-by-Step Setup Guide

**For non-technical users.** Every click described. No coding experience assumed.

**Total time:** about 25-30 minutes, split across 9 steps.

---

## Before you start

You need:

- A working computer with a modern browser (Chrome, Edge, Firefox, or Safari all work)
- The folder **`pareas_engagement_trello`** with these 7 files inside:
  - `connector.html`
  - `engagement.html`
  - `settings.html`
  - `services.xlsx`
  - `icon.svg`
  - `pareas_logo_small.png`  *(logo shown in the sidebar header)*
  - `README.md`  *(optional)*
- Your existing Trello account (the same one where your Leads board lives)
- An email address you can check

Put the folder somewhere you can easily find it — your Desktop is fine for now.

---

## STEP 1 — Create a GitHub account (5 minutes)

GitHub is a free service from Microsoft that hosts files on the internet. We use it because it gives us a free HTTPS address, which is what Trello requires.

**1.1** Open your browser and go to: `https://github.com`

**1.2** Top-right corner: click the button labelled **Sign up**

**1.3** Type your email address. Click **Continue**.

**1.4** Create a password (at least 15 characters, or 8 with a number and a lowercase letter). Write it down somewhere safe.

**1.5** Choose a username. This becomes part of your Power-Up URL forever, so pick something clean.

Good examples: `pareas-consulting`, `npareas`, `pareas-cy`
Avoid: spaces, periods, emoji, capital letters (GitHub will complain)

Write your chosen username here so you don't forget:

`_____________________________________`

**1.6** GitHub shows a simple visual puzzle (click an object, verify you're human). Solve it.

**1.7** Click **Create account**.

**1.8** Check your email. GitHub sent an 8-digit code. Type it on the GitHub page.

**1.9** GitHub asks about team size, interests, etc. You can click **Skip personalization** at the bottom, or answer however you like — it doesn't affect anything.

**1.10** You should now see your GitHub dashboard: a mostly empty page with a green button somewhere saying **Create repository** or **Start a repository**.

✅ **Checkpoint:** You are logged into GitHub.

---

## STEP 2 — Create a repository (3 minutes)

A "repository" (or "repo") is a folder on GitHub. Think of it as a Google Drive folder that lives on GitHub.

**2.1** On your dashboard, click the green **Create repository** button, or go directly to: `https://github.com/new`

**2.2** **Repository name** field: type exactly:

`pareas-engagement`

(Lowercase, hyphen, no spaces. You can pick a different name if you want, but keep the rules: lowercase, no spaces, no special characters except hyphens.)

**2.3** Description (optional): type anything, e.g. `Pareas Consulting engagement letter Trello Power-Up`.

**2.4** **Public / Private** toggle: leave **Public** selected. This is required for free GitHub Pages to work.

**2.5** **Add a README file:** tick this checkbox. It just creates a placeholder file so your repo isn't empty.

**2.6** Everything else: leave alone.

**2.7** Scroll down. Click the green **Create repository** button.

**2.8** You should now see a page titled something like:

`your-username / pareas-engagement`

With a list showing just the `README.md` file.

✅ **Checkpoint:** Your repo exists. Its web address is `https://github.com/your-username/pareas-engagement`.

---

## STEP 3 — Upload your 6 files (5 minutes)

**3.1** On your repo's main page, look for the **Add file** button (top-right area of the file list, it's a small blue or white button).

**3.2** Click **Add file**. A small menu drops down. Click **Upload files**.

**3.3** You're now on an upload page with a large dashed box saying "Drag files here or choose your files".

**3.4** Open your computer's file explorer. Navigate to the `pareas_engagement_trello` folder.

**3.5** Select all 7 required files inside:
- Click the first file
- Hold **Ctrl** (Windows) or **Cmd** (Mac)
- Click each of the other 5 files so all 6 are highlighted
- Or just press **Ctrl+A** / **Cmd+A** if the folder has only those 6 files

**3.6** Drag all 6 highlighted files into the big dashed box in the GitHub browser tab.

Each file shows a small progress bar. Wait until all say "✓" or 100%.

**3.7** Scroll down the page to the **Commit changes** section.

**3.8** You can leave the commit message empty, or type `Initial upload`.

**3.9** Click the green **Commit changes** button.

**3.10** GitHub processes the upload (usually under 5 seconds). You're returned to the repo page.

**3.11** You should now see a file list with at least 7 entries:
- `README.md` (the placeholder GitHub made — we'll overwrite it)
- `connector.html`
- `engagement.html`
- `icon.svg`
- `services.xlsx`
- `settings.html`
- `README.md` (yours, if you uploaded it)

If `README.md` appears twice or you get a warning, GitHub asks how to handle the conflict — choose "Replace existing" or accept the overwrite.

✅ **Checkpoint:** Your 6 files are inside the repo.

---

## STEP 4 — Turn on GitHub Pages (2 minutes + a short wait)

GitHub Pages is the service that turns your repo files into a website. It's free. We just need to flip a switch.

**4.1** On your repo page, look at the top row of tabs: **Code**, **Issues**, **Pull requests**, **Actions**, **Projects**, **Wiki**, **Security**, **Insights**, **Settings**. Click **Settings** (far right — on small screens it may be hidden under `...`).

**4.2** On the Settings page, look at the **left sidebar**. Scroll down until you find the section **Code and automation**. Under it, click **Pages**.

**4.3** You're now on the Pages settings page.

**4.4** Find the section **Build and deployment** > **Source**. It's a dropdown. Click it and choose:

`Deploy from a branch`

**4.5** Below that, a new section appears: **Branch**. Two dropdowns side by side.

- First dropdown: select `main`
- Second dropdown: leave as `/ (root)`

**4.6** Click the small **Save** button to the right of those dropdowns.

**4.7** A thin grey banner appears saying "GitHub Pages source saved."

**4.8** Now wait **30–60 seconds** for GitHub to build your site.

**4.9** Refresh the page (F5 or Ctrl+R / Cmd+R).

**4.10** At the **top of the Pages settings page**, you should now see a green banner:

> **Your site is live at** `https://your-username.github.io/pareas-engagement/`

(Your URL uses your own username, not the words "your-username".)

**🔑 WRITE THIS URL DOWN.** You'll need it in Step 6.

`_____________________________________________________________________`

If you don't see the green banner:
- Wait another minute, refresh again. First-time builds can take up to 5 minutes.
- Check that Source is still set to `Deploy from a branch` with `main` selected.

✅ **Checkpoint:** Your site is live.

---

## STEP 5 — Verify the URL actually works (1 minute)

**5.1** Open a new browser tab.

**5.2** Paste your URL and add `connector.html` at the end. Like this:

`https://your-username.github.io/pareas-engagement/connector.html`

Press Enter.

**5.3** You should see a page with the text:

> Pareas Consulting · Engagement Letter Power-Up · connector endpoint.

If yes → great, continue to Step 6.

If you get a "404 Not Found" page:
- Wait 2 more minutes, refresh. First builds sometimes take longer.
- Check you typed the URL correctly (no typos, ends with `.html`).
- Check in GitHub that the file `connector.html` exists in your repo.

**5.4** In another tab, test: `https://your-username.github.io/pareas-engagement/engagement.html`

You should see the full engagement creator interface — the same sidebar and preview you see when you open the standalone HTML on your computer, but now served from the internet.

✅ **Checkpoint:** Your Power-Up code is reachable at a public HTTPS URL.

---

## STEP 6 — Register the Power-Up in Trello (5 minutes)

Now we tell Trello "here's a Power-Up at this URL, please use it."

**6.1** Open a browser tab and go to: `https://trello.com/power-ups/admin`

**6.2** Log in with your Trello account (the same account where your Leads board is).

**6.3** Top-right: click the blue **+ New** button. (Or it may say "New Power-Up".)

**6.4** A form appears. Fill it in exactly like this:

| Field | What to enter |
|-------|---------------|
| **Workspace** | Choose the workspace your Leads board belongs to. If the dropdown is empty, you need to create a workspace first at trello.com (any name, free tier is fine). |
| **New Power-Up or Integration Name** | `Pareas Engagement` |
| **Iframe connector URL** | Your URL from Step 4, ending in `/connector.html`. Example: `https://pareas-consulting.github.io/pareas-engagement/connector.html` |
| **Email** | Your email address |
| **Support contact** | Same email |
| **Author** | `Pareas Consulting` or your name |

The **Iframe connector URL** is the single most important field. Copy and paste carefully.

**6.5** Click **Create** (green button at the bottom).

**6.6** You're now on your Power-Up's admin page. Look at the **left sidebar**. Click **Capabilities**.

**6.7** You see a list of capabilities (features) Power-Ups can have. Scroll through and tick the checkboxes next to:

- `card-buttons`
- `card-badges`
- `card-detail-badges`
- `authorization-status`
- `show-authorization`

Some capabilities ask for a URL when you enable them — leave those fields empty or fill in the same connector URL as before if prompted.

**6.8** Scroll to the bottom. Click **Save**.

**6.9** (Optional, but recommended) In the left sidebar click **Basic information**. Upload an icon: click **Choose file** and pick `icon.svg` from your folder. Click **Save** at the bottom.

✅ **Checkpoint:** The Power-Up is registered in Trello.

---

## STEP 7 — Install the Power-Up on your board (1 minute)

**7.1** Go to `https://trello.com` and open the board where you want the Power-Up (your Leads board).

**7.2** Top-right of the board: click **Power-Ups** (there may be an icon — a small square icon).

**7.3** A panel opens on the right. Click **Add Power-Ups** (green button).

**7.4** A dialog opens with tabs across the top: **All**, **Featured**, **Made by Trello**, ..., **Custom**.

Click **Custom**.

**7.5** You should see **Pareas Engagement** in the list. Click the **Add** button next to it.

**7.6** You may be asked "Enable custom Power-Up?" — click **Enable**.

**7.7** Close the panel (click the X).

✅ **Checkpoint:** The Power-Up is installed on your board.

---

## STEP 8 — Configure your Trello API key and token (3 minutes)

The **Engagement Letter** button works now, but attaching files to cards and updating card descriptions requires your personal Trello API access. You set this up once per user.

**8.1** Open a new tab: `https://trello.com/app-key`

**8.2** Near the top you see a big box with your **API Key** — a string of 32 characters.

Select it (click in the box, press **Ctrl+A** / **Cmd+A**) and copy (**Ctrl+C** / **Cmd+C**).

**8.3** Paste it somewhere temporary (a blank email, Notes app, Word document) so you don't lose it.

**8.4** Go back to the app-key page. A sentence says:

> You can manually generate a Token for yourself from the Trello web app. [Token]

Click the word **Token** (it's a blue link).

**8.5** A new page opens: "Pareas Engagement is requesting access to your Trello account." Scroll down. Click the green **Allow** button.

**8.6** You're redirected to a page showing a long string of 64 characters — your **Token**. Copy it and paste it next to your API Key in your temporary note.

**8.7** Go back to your Trello board.

**8.8** Top-right of the board, click **Show menu** (or the three-dots icon). In the menu click **Power-Ups**.

Find **Pareas Engagement** in the list. Click the three-dots next to it → **Edit Power-Up Settings**. (Or: on the board, click directly on the Power-Up name if it appears in the sidebar.)

**8.9** A small popup opens titled "Pareas Engagement — Settings".

**8.10** Paste your API Key in the first field. Paste your Token in the second field.

**8.11** Click **💾 Αποθήκευση**.

A green checkmark "✅ Αποθηκεύτηκαν" flashes, and the popup closes.

✅ **Checkpoint:** Credentials saved. You only do this once — they persist between sessions.

---

## STEP 9 — Test the full flow (2 minutes)

**9.1** On your board, open any card (create a test one if needed, e.g. "Test Client — John Doe").

**9.2** On the card back, look for the **Power-Ups** section. You should see a button:

> 📋 Engagement Letter

Click it.

**9.3** A full-screen modal opens inside Trello. The engagement creator appears. The client field is already pre-filled with "Test Client — John Doe" (or whatever the card title is).

**9.4** Fill in some test data:
- Pick 2-3 services in the list
- Enter a discount, e.g. 5%
- Leave Success Fee on

**9.5** Click the gold **⚡ Δημιουργία Επιστολής** button. The letter preview renders on the right.

**9.6** Click **🗂 Επισύναψη στην Καρτέλα** (the button right below the gold one).

You should see a toast:

> ⏳ Επισύναψη στην καρτέλα...

Then:

> ✅ Engagement letter attached to card

The modal closes automatically.

**9.7** Back on the card, scroll down. You should see:
- A new **Attachment**: `Engagement_Test_Client_2026-04-18.html` (click it to open the polished letter in a new tab)
- The **card description** has a structured summary (client, fee breakdown, services, link to attachment)

**9.8** Close the card. Look at it from the board view. On the card front:

> 📋 €3.500

A yellow badge shows the total fee at a glance.

🎉 **Congratulations. You're done.**

---

## What to do day-to-day

- **Open a client card** → click **Engagement Letter** → fill in → **Επισύναψη στην Καρτέλα**. The attachment and badge appear.
- **Come back later** → same button → form restores all your previous values → edit → attach again (it replaces the old attachment).

---

## Updating prices

1. On your computer, open `services.xlsx`, edit prices, save.
2. Go to your GitHub repo: `https://github.com/your-username/pareas-engagement`
3. Click the file `services.xlsx` in the list.
4. Top-right of the file view: click the **pencil icon** → you'll get an error "This file cannot be edited" (it's binary).
5. Instead: go back to the repo main page. Click **Add file** → **Upload files** → drag the new `services.xlsx` → GitHub asks "Replace existing file?" → yes → **Commit changes**.
6. Within 30 seconds the updated prices are live. Re-open any Power-Up modal to see them.

---

## Troubleshooting

### "404 Not Found" when testing the URL
- Wait 1-2 more minutes and refresh. First builds can be slow.
- In your repo, go to **Settings → Pages** and confirm you see a green "Your site is live" banner.
- Confirm your files are in the root of the repo, not inside a subfolder.

### Trello says "This Power-Up failed to load" or the modal is blank
- Your connector URL is wrong. Check in the Trello admin — must end in `/connector.html` exactly.
- Your repo is private. Check Settings → General → Danger Zone. It must say "This repository is public".

### Clicking the button shows a blank modal
- Open browser developer tools (press **F12**, click **Console** tab).
- Look for red error lines.
- Most common error: "Failed to load services.xlsx" — make sure you uploaded all 6 files.

### "Δεν έχεις ρυθμίσει API Key/Token"
You skipped Step 8. Redo it.

### Attachment upload fails with "401" or "403"
Your Trello token was revoked or expired. Regenerate it from `https://trello.com/app-key` and paste again in settings.

### I need to delete and start over
In your repo: **Settings** → scroll all the way down to "Danger Zone" → **Delete this repository** → type the name to confirm. Then redo from Step 2.

### Someone found my repo and downloaded services.xlsx
This is the privacy tradeoff we discussed. Options:
- Rename the repo to something unguessable (e.g. `pareas-x9k2m-engagement`). Update the URL in Trello admin.
- Migrate to Cloudflare Pages with Access (private, but more setup — ask for the guide).

---

## Glossary

- **Repository / Repo:** a folder on GitHub containing files.
- **Commit:** saving a new version of files to GitHub.
- **Branch:** a parallel version line. We only use the "main" branch.
- **GitHub Pages:** the free feature that serves your repo as a website.
- **Iframe:** a web page embedded inside another page. Trello loads Power-Ups as iframes.
- **Power-Up:** a Trello extension that adds features to boards/cards.
- **Capability:** a specific feature type a Power-Up can implement (card buttons, badges, etc.).
- **API:** the machine-to-machine interface Trello exposes so your Power-Up can attach files and edit cards.

---

## Files and their roles

| File | What it does |
|------|-------------|
| `connector.html` | The URL Trello calls. Declares the Power-Up's capabilities. User never sees it directly. |
| `engagement.html` | The full creator UI. Opens inside the Trello modal when you click the button. |
| `settings.html` | The small popup for entering your API Key/Token. |
| `services.xlsx` | Your price catalog. Edit this to update prices. |
| `icon.svg` | The icon shown on the button. |
| `README.md` | This and other reference docs. Not loaded by Trello. |

You **do not** need to understand what's inside these files. Just keep all 6 in the repo together. Never delete `connector.html` without replacing it — that's what Trello uses to find everything else.

---

**Done.** Total elapsed: about 25-30 minutes. Save this guide somewhere you can find it if you ever need to set up another board or redo a step.
