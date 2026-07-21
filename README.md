# Miller³ Consulting Website — Deploy to GitHub + Vercel + GoDaddy

## What's in this folder
15 self-contained static HTML pages (all images embedded as base64 — nothing external needed):
`index.html` (homepage), `about.html`, `case-studies.html`, `clients.html`, `contact.html`,
`founder.html`, `history.html`, `insights.html`, `pip.html`, `service-data.html`,
`service-economic.html`, `service-outreach.html`, `service-procurement.html`,
`service-supplier.html`, `team.html`

No build step, no JavaScript framework — just plain HTML files. This is simpler to deploy than the P2P site.

## 1. Create a new GitHub repo
- github.com → **+** → **New repository**
- Name it `miller3-website`
- Keep it **Public**, don't add a README
- **Create repository**

## 2. Upload the files
- On the repo page → **Add file** → **Upload files**
- Drag in all 15 `.html` files from this folder
- **Commit changes**

## 3. Deploy with Vercel
- vercel.com → **Add New...** → **Project**
- Find `miller3-website` → **Import**
- Framework preset: **Other**, leave build settings blank
- **Deploy**

## 4. Connect your GoDaddy domain (www.miller3group.com)
- In the Vercel project → **Settings** → **Domains**
- Type `miller3group.com` → since you already own it, click **Add Existing** (not "Buy")
- Vercel will show DNS records (likely an A record for `@` and/or a CNAME for `www`)
- In GoDaddy: **My Products** → `miller3group.com` → **DNS**
- ⚠️ Check for GoDaddy's default placeholder A record (Data: "WebsiteBuilder Site") on `@` — delete it, it blocks other changes from saving (we ran into this with the P2P domain)
- Add/edit the records to match exactly what Vercel shows
- Wait for the green checkmark in Vercel (can take minutes to a few hours)

## Notes
- Two files from the original zip (`Miller3 Consulting - Homepage.html` and `Miller3 Consulting - Procurement Optimization.html`, sitting outside the WEBSITE folder) were left out — they look like earlier draft exports, not part of this final 15-page set. Flag if that's wrong.
- Footer links and contact info: worth double-checking these are final before pointing the real domain here (flagged as pending polish items in earlier sessions).
