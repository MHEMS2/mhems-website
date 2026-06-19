# MHEMS Website — Setup Guide

## What You Have

A complete website built with Hugo (a static site generator) + Decap CMS. Once deployed:
- Your team edits content at **morristownhamblenems.org/admin**
- Changes go live automatically in ~30 seconds
- No code, no FTP, no developers needed for day-to-day updates

---

## One-Time Setup (Do This Once)

### Step 1 — Create a GitHub Account (if you don't have one)
1. Go to **github.com** and sign up for a free account
2. Verify your email address

### Step 2 — Create a New GitHub Repository
1. Click the **+** icon (top right) → **New repository**
2. Name it: `mhems-website`
3. Set it to **Private**
4. Click **Create repository**
5. On the next screen, click **Upload files**
6. Upload the entire contents of the `mhems-site` folder (everything inside it)
7. Click **Commit changes**

### Step 3 — Connect to Netlify
1. Go to **netlify.com** and log in (or create a free account)
2. Click **Add new site** → **Import an existing project**
3. Choose **GitHub** and authorize Netlify
4. Select your `mhems-website` repository
5. Build settings should auto-fill (Hugo, `public` folder) — leave them as-is
6. Click **Deploy site**
7. Your site will build in about 60 seconds — Netlify gives you a temporary URL to preview it

### Step 4 — Point Your Domain to Netlify
1. In Netlify, go to **Domain settings** → **Add custom domain**
2. Enter: `morristownhamblenems.org`
3. Netlify will show you nameservers (looks like: `dns1.p01.nsone.net`)
4. Log in to wherever you registered your domain (GoDaddy, Namecheap, etc.)
5. Find **DNS / Nameservers** settings and replace them with Netlify's nameservers
6. DNS propagation takes 24–48 hours — your old Yola site stays up during this time

### Step 5 — Enable Netlify Identity (for CMS login)
1. In your Netlify dashboard, go to **Site settings** → **Identity**
2. Click **Enable Identity**
3. Under **Registration**, change to **Invite only** (so only your team can log in)
4. Scroll to **Services** → **Git Gateway** → click **Enable Git Gateway**

### Step 6 — Set Up Form Email Notifications
1. In Netlify, go to **Forms** (in the top navigation)
2. After your first contact form submission, you'll see "contact" listed
3. Click it → **Form notifications** → **Add notification** → **Email notification**
4. Add these three emails:
   - dhouseright@mhems.com
   - cthompson@mhems.com
   - msallah@mhems.com
5. Save

### Step 7 — Invite Your Team to the CMS
1. In Netlify → **Identity** → **Invite users**
2. Enter the email addresses of anyone who needs to edit the site
3. They'll receive an email to set a password
4. They log in at: **morristownhamblenems.org/admin**

---

## Things to Update First

After the site is live, log into the admin panel and update:

1. **Contact page** — Replace the placeholder phone numbers with your real ones
2. **Employment page** — Paste your Google Doc URL into the "Google Doc URL" field
3. **Administration page** — Add your bio and optionally a photo
4. **Home page** — Customize the hero headline and mission statement if desired

---

## Day-to-Day: How to Edit the Site

1. Go to **morristownhamblenems.org/admin**
2. Log in with your email and password
3. You'll see the editor with these sections:
   - **News** — Add/edit news posts and announcements
   - **Pages** — Edit the Home, About, Administration, Employment, Contact pages
   - **Gallery** — Upload photos
4. Make your changes, hit **Publish**
5. Site updates automatically in about 30 seconds

---

## Adding Your Google Doc (Employment Page)

1. Open your Google Doc
2. Click **File** → **Publish to the web** → **Link** → **Publish**
3. Copy the link
4. In the CMS admin, go to **Pages** → **Employment Page**
5. Paste the link into the **Google Doc URL** field
6. Publish

---

## Need Help?

- Netlify docs: **docs.netlify.com**
- Decap CMS docs: **decapcms.org/docs**
- Hugo docs: **gohugo.io/documentation**

For technical changes beyond content editing (layout, colors, new pages), reach out to your developer or use Claude to help make specific code changes.
