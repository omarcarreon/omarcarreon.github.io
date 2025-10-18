# Deployment Guide to GitHub Pages

Follow these step-by-step instructions to deploy your portfolio to GitHub Pages.

## Prerequisites

- GitHub account
- Git installed on your computer
- Your portfolio code ready (already done! ✅)

## Step-by-Step Deployment

### 1. Create a GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the **+** icon in the top right → **New repository**
3. Repository name: `portfolio`
4. Make it **Public**
5. **Do NOT** initialize with README, .gitignore, or license (we already have these)
6. Click **Create repository**

### 2. Push Your Code to GitHub

Open your terminal in the portfolio directory and run:

```bash
# Add all files to git
git add .

# Create your first commit
git commit -m "Initial portfolio setup"

# Add your GitHub repository as remote
git remote add origin https://github.com/omarcarreon/portfolio.git

# Rename branch to main (if needed)
git branch -M main

# Push to GitHub
git push -u origin main
```

### 3. Deploy to GitHub Pages

Still in your terminal, run:

```bash
npm run deploy
```

This command will:
- Build your Astro site
- Create a `gh-pages` branch
- Push the built site to that branch

### 4. Enable GitHub Pages

1. Go to your repository on GitHub: `https://github.com/omarcarreon/portfolio`
2. Click on **Settings** (gear icon in the top menu)
3. In the left sidebar, click **Pages** (under "Code and automation")
4. Under **Source**, select:
   - Branch: `gh-pages`
   - Folder: `/ (root)`
5. Click **Save**

### 5. Wait for Deployment

- GitHub will show a message: "Your site is ready to be published"
- Wait 1-2 minutes for the initial deployment
- Your site will be live at: **https://omarcarreon.github.io/portfolio**

## Updating Your Portfolio

Whenever you make changes to your portfolio:

```bash
# Make your changes, then:
git add .
git commit -m "Description of your changes"
git push origin main

# Deploy the updates
npm run deploy
```

Changes will be live in 1-2 minutes!

## Testing Before Deployment

Always test your changes locally before deploying:

```bash
# Start dev server
npm run dev

# Or build and preview
npm run build
npm run preview
```

## Troubleshooting

### Site shows 404 or broken styles

- Make sure you've selected the `gh-pages` branch in GitHub Pages settings
- Verify the `base: '/portfolio'` setting in `astro.config.mjs` matches your repo name
- Wait a few minutes after deployment

### Deployment fails

- Make sure you have committed all your changes
- Check that you have internet connection
- Try deleting the `gh-pages` branch on GitHub and run `npm run deploy` again

### Changes not showing up

- Clear your browser cache (Ctrl+Shift+R or Cmd+Shift+R)
- Wait a few minutes for GitHub Pages to update
- Check that you ran `npm run deploy` (not just `git push`)

## Need Help?

If you encounter issues:
1. Check the [GitHub Pages documentation](https://docs.github.com/en/pages)
2. Review the [Astro deployment guide](https://docs.astro.build/en/guides/deploy/github/)
3. Make sure all commands completed without errors

---

Good luck with your portfolio! 🚀

