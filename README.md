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

1. Push this repository to GitHub
2. Go to **Settings > Pages** in your GitHub repository
3. Under **Source**, select **GitHub Actions**
4. The workflow will automatically deploy when you push to the `main` or `master` branch
5. Your site will be available at `https://yourusername.github.io/price-pirate-web/`

### Option 2: Direct GitHub Pages (Simple)

1. Push this repository to GitHub
2. Go to **Settings > Pages** in your GitHub repository
3. Under **Source**, select **Deploy from a branch**
4. Select the branch (usually `main` or `master`) and folder (`/root`)
5. Your site will be available at `https://yourusername.github.io/price-pirate-web/`

### Notes

- Make sure the repository name matches the URL path. If your repository is named `price-pirate-web`, the privacy page will be at `/price-pirate-web/privacy.html`
- The GitHub Actions workflow (`.github/workflows/deploy.yml`) will automatically run on every push to `main` or `master`
- You can also manually trigger the deployment using the "Run workflow" button in the Actions tab
