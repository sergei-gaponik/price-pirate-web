# price-pirate-web

A simple static website for PricePirate, hosted on GitHub Pages.

## Structure

- `index.html` - Main page that redirects to `/privacy`
- `privacy.html` - Privacy policy page
- `styles.css` - Stylesheet for the website
- `assets/pricepirate-logo.png` - Logo image

## GitHub Pages Setup

### Option 1: Using GitHub Actions (Recommended)

This repository includes a GitHub Actions workflow that automatically deploys to GitHub Pages.

**⚠️ CRITICAL: You MUST enable Pages manually FIRST before the workflow can run!**

**Step-by-Step Setup:**

1. **Push repository to GitHub** (if not already done):
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

2. **Enable GitHub Pages** (REQUIRED FIRST STEP):
   - Go to your repository on GitHub
   - Click **Settings** (top menu)
   - Click **Pages** (left sidebar)
   - Under **"Source"**, select **"GitHub Actions"** (NOT "Deploy from a branch")
   - This creates the `github-pages` environment automatically
   - **Do NOT skip this step** - the workflow will fail without it!

3. **Configure Workflow Permissions**:
   - Still in **Settings**, click **Actions** → **General** (left sidebar)
   - Scroll down to **"Workflow permissions"**
   - Select **"Read and write permissions"**
   - ✅ Check **"Allow GitHub Actions to create and approve pull requests"**
   - Click **Save** button

4. **Trigger the workflow**:
   - Make any small change (or the workflow will run automatically on next push)
   - Go to **Actions** tab to see the workflow run
   - Wait for it to complete - your site will be live!

5. **Your site URL**:
   - `https://yourusername.github.io/price-pirate-web/`
   - The workflow will show the URL in the deployment step

### Option 2: Direct GitHub Pages (Simple)

1. Push this repository to GitHub
2. Go to **Settings > Pages** in your GitHub repository
3. Under **Source**, select **Deploy from a branch**
4. Select the branch (usually `main` or `master`) and folder (`/root`)
5. Your site will be available at `https://yourusername.github.io/price-pirate-web/`

### Troubleshooting Deployment Failures

If the GitHub Actions deployment fails, check the following:

1. **Repository Settings**: 
   - Go to **Settings > Pages**
   - Make sure **Source** is set to **GitHub Actions** (not "Deploy from a branch")
   - The `github-pages` environment should be created automatically

2. **Repository Permissions**:
   - Go to **Settings > Actions > General**
   - Under "Workflow permissions", ensure "Read and write permissions" is selected
   - Check "Allow GitHub Actions to create and approve pull requests"

3. **Check Workflow Logs**:
   - Go to the **Actions** tab in your repository
   - Click on the failed workflow run
   - Review the error messages in the logs

4. **Common Issues**:
   - If you see "Environment protection rules", you may need to approve the deployment in the Environments section
   - Make sure you're pushing to the `main` or `master` branch
   - Ensure the workflow file is in `.github/workflows/deploy.yml`

### Notes

- Make sure the repository name matches the URL path. If your repository is named `price-pirate-web`, the privacy page will be at `/price-pirate-web/privacy.html`
- The GitHub Actions workflow (`.github/workflows/deploy.yml`) will automatically run on every push to `main` or `master`
- You can also manually trigger the deployment using the "Run workflow" button in the Actions tab
- The `.nojekyll` file ensures GitHub Pages doesn't try to process the site with Jekyll
