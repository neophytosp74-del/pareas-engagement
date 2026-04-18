# Pareas Engagement Letter — Trello Power-Up

A Trello Power-Up that embeds the Pareas engagement-letter creator directly into any Trello card. Click a button on a card → the creator opens as a full-screen modal pre-filled with the client's name (from the card title) → generate the letter → attach it to the card with one click. A yellow badge appears on the card showing the total fee.

---

## What's in this folder

| File | Role |
|------|------|
| `connector.html` | The Power-Up connector URL. This is what you give Trello when you register the Power-Up. Trello loads this invisibly to discover the card button, card badges, and settings popup. |
| `engagement.html` | The full engagement creator that opens inside the Trello modal. Same UI as the standalone v3, plus "Attach to Card". Works both inside Trello and standalone. |
| `settings.html` | Small popup where the user pastes their Trello REST API key + token (needed to upload attachments and edit the card description). Values are stored per-user via Trello's `t.storeSecret` so only that user can read them back. |
| `services.xlsx` | The same Excel catalog as v3. The iframe auto-loads it from this same hosting URL. Update it any time — refresh the modal to pick up new prices. |
| `icon.svg` | Icon shown on the card button. Uncolored — Trello tints it to match the theme. |

---

## Step 1 — Put the files on a public HTTPS URL

Trello will not load a Power-Up from `file://` or from `http://` — it must be HTTPS. Pick one option below. Each gives you a URL that looks like `https://something.example.com/` — I will call that your **BASE URL**.

### Option A — GitHub Pages (recommended; free, 5 minutes)

1. Create a free GitHub account if you do not have one.
2. Create a new public repository. Name it anything, e.g. `pareas-engagement`.
3. Upload all five files (`connector.html`, `engagement.html`, `settings.html`, `services.xlsx`, `icon.svg`) to the root of the repo. The web interface — "Add file → Upload files" — is fine.
4. In the repo, go to **Settings → Pages**.
5. Under "Build and deployment", set **Source** to "Deploy from a branch", **Branch** to `main` and folder to `/ (root)`, then click **Save**.
6. Wait 30–60 seconds. GitHub Pages will show a green banner with your URL. It will look like `https://yourusername.github.io/pareas-engagement/`.
7. Open that URL in a browser to confirm the files are reachable. You should see the landing text from `connector.html`. Open `engagement.html` directly to see the full UI.

Your **BASE URL** is `https://yourusername.github.io/pareas-engagement/`.

### Option B — Vercel / Netlify / Cloudflare Pages (also free)

1. Sign up for the provider of your choice.
2. Create a new project, drag-and-drop this folder into the deploy interface, and deploy.
3. The provider gives you a URL. That is your **BASE URL**.

### Option C — Your own server

Upload the five files to any folder served over HTTPS. The folder's public URL is your **BASE URL**.

---

## Step 2 — Register the Power-Up

1. Go to <https://trello.com/power-ups/admin> and sign in with the Trello account that will own the Power-Up.
2. Click **New** to create a new Power-Up.
3. Fill in the form:
   - **New Power-Up or Integration Name:** `Pareas Engagement`
   - **Workspace:** pick the workspace your Leads board belongs to
   - **Iframe connector URL:** `<BASE URL>connector.html` — for example `https://yourusername.github.io/pareas-engagement/connector.html`. This is the single most important field.
   - **Email / Support contact / Author:** fill with your own
4. Click **Create**.
5. On the next screen, click **Capabilities** in the left sidebar and tick:
   - `card-buttons`
   - `card-badges`
   - `card-detail-badges`
   - `authorization-status`
   - `show-authorization`
   Save.
6. Optional but nice: under **Basic information**, upload an icon (you can use `icon.svg` from this folder) and add a short description.

You do not need an API key here — that's a separate concept. The REST API credentials go in the Power-Up's own settings (step 4).

---

## Step 3 — Install it on your board

1. Open the Trello board where you want to use the Power-Up (e.g. your Leads board).
2. Click **Power-Ups** (top right of the board) → **Add Power-Up**.
3. Switch to the **Custom** tab. Your `Pareas Engagement` Power-Up should be listed.
4. Click **Add**.

---

## Step 4 — Save your Trello REST API credentials inside the Power-Up

The attach-to-card feature needs to upload a file and edit the card's description. Those two operations require a REST API key and a user token. You save them once, per user, and they live encrypted inside Trello (via `t.storeSecret`) — no other user sees them.

1. Go to <https://trello.com/app-key>. Copy the **API Key** (first field).
2. On the same page, click the **Token** link to generate a personal token. Approve access. Copy the long token string.
3. In Trello, on the board where you installed the Power-Up, click the Power-Up name in the right sidebar or click **Show menu → Power-Ups → Pareas Engagement → Edit Power-Up Settings**. A popup opens (`settings.html`).
4. Paste the API Key and Token. Click **Αποθήκευση**. Done.

You never need to re-enter this unless you manually clear it.

---

## Step 5 — Use it

1. Open any card on the board.
2. On the card back, in the **Power-Ups** section, click **Engagement Letter**.
3. The full creator opens in a modal, with the client name pre-filled from the card title.
4. Fill in the rest (banks, services, discount, success fee, payment schedule), click **⚡ Δημιουργία Επιστολής** to preview.
5. Click **🗂 Επισύναψη στην Καρτέλα**. Three things happen:
   - The HTML letter is uploaded as an attachment on the card.
   - The card description gets a structured summary (client, fee breakdown, services, link to the attachment) between `<!--PAREAS_ENGAGEMENT-->` markers.
   - A compact summary is stored per-card so the badge can display the total.
6. Close the modal. On the card front you now see a yellow badge: **📋 €3.500** (or whatever the total is).
7. Re-open the same card later, click the button again, and the form restores the previous values so you can revise.

---

## Updating prices or adding services

Edit `services.xlsx` the way you already do. Upload the updated file to the same hosting folder (overwriting the old one). Inside any open Power-Up modal, click **🔄 Ανανέωση** to force a fresh load — or just reopen the modal.

---

## Troubleshooting

**The Power-Up does not appear on the board.**
Make sure you installed it on the specific board under the Custom tab. Creating the Power-Up in the admin only registers it — you still have to add it to the board.

**The button appears but clicking it does nothing / shows a blank modal.**
Open the browser devtools console inside the Trello page. Common causes:
- The **Iframe connector URL** in the admin points to the wrong path. Open that URL in a new tab — if the browser shows a 404, fix the URL.
- Your hosting is not serving HTTPS. `http://` will not load. GitHub Pages, Vercel, Netlify, Cloudflare Pages all serve HTTPS automatically.
- Mixed-content error: every URL the iframe loads must be HTTPS. The CDN scripts in the HTML already are.

**"⚠ Δεν έχεις ρυθμίσει API Key/Token" when I click Attach.**
Do step 4 above.

**Attachment upload fails with 401 or 403.**
Your token is wrong or was revoked. Re-generate from `trello.com/app-key` and paste again in settings.

**services.xlsx does not load inside Trello.**
Confirm it is in the same folder as `engagement.html` on your hosting URL. Open `<BASE URL>services.xlsx` directly in a browser — it should download. Clear the Power-Up's cached copy via the **🗑 Cache** button inside the Ρυθμίσεις tab of the modal.

**I updated `services.xlsx` but the modal still shows old prices.**
The browser cached the file. Click **🔄 Ανανέωση** inside the modal, or hard-refresh (Ctrl-Shift-R). The Power-Up fetches with `cache: 'no-store'` but some intermediate caches can still linger.

**The badge shows an old fee after I redid the letter.**
Click Attach again — the badge updates from the saved summary. If the badge is stuck, close and reopen the card.

---

## How does this relate to the standalone `engagement_creator_v3.html`?

The standalone v3 on your computer is unchanged and still works exactly the same. The Power-Up is a second, parallel deployment that reuses the same Excel catalog schema. You can use either — or both.

- Standalone: best for quick offline drafting, no Trello context needed.
- Power-Up: best when the engagement lives inside a Trello pipeline and you want attachment + badge automation.

Both produce identical letter output. If you edit `services.xlsx` in one place, copy it to the other (or keep both folders in sync via a shared drive).

---

## Security notes

- Your REST API token is stored only inside Trello, scoped to your user, via `t.storeSecret`. Other board members cannot read it.
- The token has your full Trello permissions. Do not paste it into anything outside `settings.html`.
- The hosted files are public — anyone who finds the URL can load the creator. They cannot see your Trello data (they would need their own token to attach anything to your board). If this is still uncomfortable, use a private hosting option that requires auth, and configure Trello's iframe CSP accordingly (more involved setup).
- No customer data is sent anywhere except to Trello's API (for attachments and description edits) and optionally EmailJS (if you use the Email button).
