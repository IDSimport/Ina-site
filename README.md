# INA Services & Logistics LLC — Website

One-page site for INA Services & Logistics LLC (yacht & pool parts distribution + maintenance).

## Files
- `index.html` — the whole site (HTML/CSS/JS in one file)
- `assets/logo.png` — your logo

## 1. Before you publish: connect the contact form
The form currently points to a placeholder:
```
action="https://formspree.io/f/YOUR_FORM_ID"
```
Go to [formspree.io](https://formspree.io), create a free account, create a new form using `info@inaservicesandlogistics.com`, and replace `YOUR_FORM_ID` in `index.html` (search for it — line is inside the `<form>` tag) with the real ID Formspree gives you.

## 2. Push to a new GitHub repo
```bash
cd ina-site
git init
git add .
git commit -m "Initial site for INA Services & Logistics LLC"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/ina-site.git
git push -u origin main
```

## 3. Turn on GitHub Pages
1. In the repo, go to **Settings → Pages**.
2. Under "Build and deployment", select **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. Save. GitHub gives you a temporary URL like `https://YOUR_USERNAME.github.io/ina-site/`.

## 4. Point your Zoho domain to GitHub Pages
In Zoho DNS (or wherever `inaservicesandlogistics.com` is managed):

**For the root domain (`inaservicesandlogistics.com`):** add these 4 A records, all pointing the root `@` to GitHub's IPs:
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**For `www.inaservicesandlogistics.com`:** add a CNAME record:
```
www  →  YOUR_USERNAME.github.io
```

Then, back in GitHub repo **Settings → Pages → Custom domain**, enter `www.inaservicesandlogistics.com` and save — this creates a `CNAME` file in your repo automatically. Check "Enforce HTTPS" once it's available (can take a few hours to activate).

DNS changes can take anywhere from a few minutes to 24-48 hours to fully propagate.

## Notes
- Colors and fonts are pulled from the INA logo (deep purple, orange/gold).
- The WhatsApp button links to +1 (504) 458-8686.
- To update text or add real photos later, just edit `index.html` directly — everything is in one file.
