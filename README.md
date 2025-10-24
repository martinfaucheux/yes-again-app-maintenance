# YesAgain App - Maintenance Page

This repository contains the static maintenance page for YesAgain App, deployed via GitHub Pages.

## 🌐 Live Page

The maintenance page is available at: `https://martinfaucheux.github.io/yes-again-app-maintenance/`

## 📋 Content

The page displays a friendly French maintenance message explaining that the server is temporarily overloaded due to high user interest in recycling and sustainable consumption.

## 🎨 Design

- **Color Scheme**: `#2596be` (Blue accent and background)
- **Responsive Design**: Optimized for both desktop and mobile devices
- **French Language**: Content is in French for the target audience

## 🚀 GitHub Pages Setup

To enable GitHub Pages for this repository:

1. Go to the repository Settings
2. Navigate to "Pages" in the sidebar
3. Under "Source", select "Deploy from a branch"
4. Choose "main" branch and "/ (root)" folder
5. Click "Save"

The page will be automatically deployed and accessible at the GitHub Pages URL.

## 🌍 Custom Domain Setup (IONOS)

To connect this GitHub Pages site to your IONOS managed domain:

### Step 1: Configure GitHub Pages Custom Domain

1. Go to your repository Settings → Pages
2. In the "Custom domain" field, enter your domain (e.g., `maintenance.yourdomain.com` or `yourdomain.com`)
3. Check "Enforce HTTPS" (recommended)
4. GitHub will create a `CNAME` file in your repository

### Step 2: Configure DNS in IONOS

#### For a subdomain (e.g., maintenance.yourdomain.com):

1. Log into your IONOS control panel
2. Go to Domains & SSL → DNS
3. Add a **CNAME record**:
   - **Name**: `maintenance` (or your chosen subdomain)
   - **Value**: `martinfaucheux.github.io`
   - **TTL**: 3600 (1 hour)

#### For apex domain (e.g., yourdomain.com):

1. In IONOS DNS settings, add **A records** pointing to GitHub's IP addresses:

   - **Name**: `@` (or leave empty)
   - **Value**: Add these four A records:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - **TTL**: 3600

2. Add a **CNAME record** for www:
   - **Name**: `www`
   - **Value**: `martinfaucheux.github.io`
   - **TTL**: 3600

### Step 3: Verification & SSL

- DNS propagation can take 24-48 hours
- GitHub will automatically provision SSL certificate once DNS is configured
- You can check DNS propagation using tools like `dig` or online DNS checkers

### 🔧 Troubleshooting

- If you get a 404 error, ensure the `CNAME` file contains your domain name
- DNS changes may take time to propagate globally
- Check that your domain is correctly configured in GitHub Pages settings

## 📝 Maintenance Message

The page includes the following message:

> **Trop d'amour pour un seul serveur**
>
> 🚧 Oups… On a dit "Oui" un peu trop fort.
>
> Vous êtes beaucoup à vouloir consommer moins et recycler plus (et c'est génial) 💚
>
> Résultat : notre serveur a paniqué et a demandé une petite pause.
>
> On revient très vite, promis !
>
> En attendant, respirez… et pensez à toutes ces déco qui n'attendent que vous ✨
