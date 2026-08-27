# TM SILK — Netlify static CMS deployment

This version uses only Netlify hosting features: Netlify Identity, Git Gateway, automatic Git-based deploys, and Netlify Forms. It has no Node.js project, server function, database, or external Worker.

## Step 1 — Put this folder on GitHub

Create an empty GitHub repository (for example `tm-silk-website`) and upload every item in this folder. Keep `admin/`, `site-data.json`, and `index.html` at the repository root.

## Step 2 — Connect it to Netlify

In Netlify, choose **Add new project** → **Import an existing project** → **GitHub**, select the new repository, and deploy with no build command and `.` as the publish directory.

## Step 3 — Turn on secure editing

In the deployed project's Netlify dashboard:

1. Open **Identity** and enable it.
2. Under **Registration preferences**, choose **Invite only**.
3. Invite the email address you will use as the administrator.
4. Open **Identity** → **Services** and enable **Git Gateway**.

## Step 4 — Edit the website

Open `https://your-site.netlify.app/admin/`, accept the invitation, and sign in. Edit Website Content and publish your changes. The CMS saves a commit to GitHub; Netlify detects it and automatically redeploys the live website.

Customer messages use Netlify Forms. View them in the Netlify dashboard under **Forms**.
