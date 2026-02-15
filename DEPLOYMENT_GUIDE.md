# How to Deploy to GitHub Pages

Follow these steps to deploy your project website to GitHub Pages:

## Step 1: Create GitHub Repository

1. Go to https://github.com and log in
2. Click the "+" icon in top right → "New repository"
3. Repository settings:
   - **Name:** `pa-agent-project` (or any name you prefer)
   - **Description:** "CS598 Prior Authorization Agent Project Website"
   - **Public** (so team members can access)
   - **DO NOT** initialize with README (we already have one)
4. Click "Create repository"

## Step 2: Upload Files

### Option A: Using GitHub Web Interface (Easiest)

1. On your new repository page, click "uploading an existing file"
2. Drag and drop these files:
   - `index.html`
   - `README.md`
3. Scroll down, add commit message: "Initial project website"
4. Click "Commit changes"

### Option B: Using Git Command Line

```bash
# Navigate to the pa-agent-website folder
cd pa-agent-website

# Initialize git repository
git init

# Add all files
git add .

# Commit files
git commit -m "Initial project website"

# Add your GitHub repository as remote (replace YOUR-USERNAME and REPO-NAME)
git remote add origin https://github.com/YOUR-USERNAME/REPO-NAME.git

# Push to GitHub
git branch -M main
git push -u origin main
```

## Step 3: Enable GitHub Pages

1. In your repository, click "Settings" (top menu)
2. Scroll down and click "Pages" (left sidebar)
3. Under "Source":
   - Select branch: `main`
   - Select folder: `/ (root)`
4. Click "Save"
5. Wait 1-2 minutes for deployment

## Step 4: Get Your Website URL

After deployment, GitHub will show your URL at the top of the Pages settings:

```
Your site is published at https://YOUR-USERNAME.github.io/pa-agent-project/
```

Copy this URL to share with your team!

## Step 5: Update README (Optional)

Edit `README.md` to replace the placeholder URL with your actual GitHub Pages URL.

## Troubleshooting

**Problem:** "Images not showing"
- **Solution:** The images are embedded as base64 in the HTML, so they should work automatically. If not, check browser console for errors.

**Problem:** "404 Page Not Found"
- **Solution:** Wait a few minutes after enabling Pages. GitHub needs time to deploy.

**Problem:** "Repository not found"
- **Solution:** Make sure repository is Public, not Private.

## Updating the Website

To make changes later:

1. Edit `index.html` locally
2. Go to your repository on GitHub
3. Click on `index.html`
4. Click the pencil icon (Edit)
5. Paste your new content
6. Commit changes
7. GitHub Pages will auto-update in 1-2 minutes

---

## Quick Summary

1. Create GitHub repo (public)
2. Upload `index.html` and `README.md`
3. Enable GitHub Pages (Settings → Pages → Source: main branch)
4. Share URL: `https://YOUR-USERNAME.github.io/REPO-NAME/`

That's it! Your team can now access the website from anywhere.
