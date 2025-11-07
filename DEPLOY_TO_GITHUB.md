# Deploy to GitHub Pages - Quick Guide

Your site is ready to deploy! Follow these steps:

## Step 1: Create GitHub Repository

1. Go to https://github.com/new
2. **Repository name**: `lumina-website` (or your preferred name)
3. **Description**: "Lumina Property Management - Conversion-Optimized Homepage"
4. **Visibility**: Choose Public or Private
5. **DO NOT** initialize with README, .gitignore, or license (we already have these)
6. Click **"Create repository"**

## Step 2: Push to GitHub

After creating the repository, GitHub will show you commands. Use these:

```bash
cd /Users/paul/dev/lumina-website
git remote add origin https://github.com/YOUR-USERNAME/lumina-website.git
git branch -M main
git push -u origin main
```

**Replace `YOUR-USERNAME` with your actual GitHub username!**

## Step 3: Enable GitHub Pages

1. In your GitHub repository, click **Settings**
2. Scroll down to **Pages** section (in left sidebar)
3. Under **Source**, select:
   - Branch: `main`
   - Folder: `/ (root)`
4. Click **Save**
5. Wait 1-2 minutes for deployment

## Step 4: Access Your Live Site

Your site will be available at:
```
https://YOUR-USERNAME.github.io/lumina-website/
```

GitHub will show you the exact URL in the Pages settings.

---

## Alternative: Quick Commands (Copy & Paste)

If you already know your GitHub username, just replace `YOUR-USERNAME` and run:

```bash
cd /Users/paul/dev/lumina-website
git remote add origin https://github.com/YOUR-USERNAME/lumina-website.git
git branch -M main
git push -u origin main
```

---

## Updating Your Live Site

After making changes:

```bash
cd /Users/paul/dev/lumina-website
git add .
git commit -m "Description of your changes"
git push
```

Changes will appear on your live site in 1-2 minutes.

---

## Troubleshooting

**"remote origin already exists"**
```bash
git remote remove origin
git remote add origin https://github.com/YOUR-USERNAME/lumina-website.git
```

**Authentication issues**
- You may need to use a Personal Access Token instead of your password
- GitHub.com → Settings → Developer settings → Personal access tokens → Generate new token

**Site not updating**
- Wait 2-3 minutes (GitHub Pages can take time)
- Check GitHub Actions tab for deployment status
- Clear browser cache and hard refresh (Cmd+Shift+R)

---

## Custom Domain (Optional)

To use your own domain (e.g., lumina-pm.com):

1. In GitHub Pages settings, add your custom domain
2. In your domain registrar (GoDaddy, Namecheap, etc.), add these DNS records:
   - A record: 185.199.108.153
   - A record: 185.199.109.153
   - A record: 185.199.110.153
   - A record: 185.199.111.153
   - CNAME record: YOUR-USERNAME.github.io

Allow 24 hours for DNS propagation.

---

## Need Help?

- GitHub Pages Docs: https://docs.github.com/en/pages
- Git Basics: https://git-scm.com/book/en/v2/Getting-Started-Git-Basics








