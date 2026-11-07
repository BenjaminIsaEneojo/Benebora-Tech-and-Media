# BeneBora Tech and Media: Website

A simple static website (HTML, CSS and a little JavaScript). No build step, so it hosts directly on GitHub Pages.

## Go live in three steps

### 1. Put the site on GitHub Pages
1. Create a new repository on GitHub (e.g. `benebora-website`).
2. Upload everything in this folder to the **root** of the repository: `index.html`, `styles.css`, `script.js`, `CNAME`, and the `assets` folder.
3. Go to **Settings > Pages**. Under **Build and deployment**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then Save.
4. After about a minute the site is live at `https://<your-github-username>.github.io/<repository-name>/`. Check it there first.

### 2. Add the DNS records for beneboratechmedia.com.ng
Log in to the registrar where you bought the domain, open its DNS management page, and add:

| Type  | Name / Host | Value |
|-------|-------------|-------|
| A     | `@`         | `185.199.108.153` |
| A     | `@`         | `185.199.109.153` |
| A     | `@`         | `185.199.110.153` |
| A     | `@`         | `185.199.111.153` |
| CNAME | `www`       | `<your-github-username>.github.io` |

Delete any existing A or CNAME records for `@` or `www` that point somewhere else (for example a registrar parking page). Some registrars write `@` as blank or as the domain name itself, and some want a trailing dot on the CNAME value. Follow whatever format their form shows.

### 3. Connect the domain in GitHub
1. In **Settings > Pages**, enter `www.beneboratechmedia.com.ng` under **Custom domain** and Save. (The `CNAME` file in this folder already contains this domain.)
2. Wait for the DNS check to pass. This can take anywhere from a few minutes to 24 hours.
3. Tick **Enforce HTTPS** once it becomes available.

Visitors who type `beneboratechmedia.com.ng` (without www) are redirected to the www version automatically.

## Before you announce the site
- The contact section shows **info@beneboratechmedia.com.ng**. Make sure this mailbox exists (your registrar or a free provider such as Zoho Mail can set it up), or change the address in `index.html`.
- The WhatsApp button uses 0708 431 4714. Change `wa.me/2347084314714` in `index.html` if you prefer the other number.

## Editing content
Everything is in `index.html`, split into clearly commented sections (`<!-- SERVICES -->`, `<!-- ACADEMY TEASER -->`, and so on). Colours and fonts are CSS variables at the top of `styles.css`.

- **Availability badge:** in the hero, delete the `<span class="badge">...</span>` line, or change its text (for example, "Booking for November").
- **Academy:** when you plan a cohort, add the start date to the course card in the Academy section.
