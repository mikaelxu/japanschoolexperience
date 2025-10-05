# Deploying Japan School Experience to Cloudflare Pages

This guide will help you deploy your Japan School Experience website to Cloudflare Pages.

## Prerequisites

- A Cloudflare account (free tier is sufficient)
- Your project pushed to a Git repository (GitHub, GitLab, or Bitbucket)

## Deployment Steps

### 1. Prepare Your Repository

Make sure your project is committed and pushed to your Git repository:

```bash
git add .
git commit -m "Prepare for Cloudflare Pages deployment"
git push origin main
```

### 2. Connect to Cloudflare Pages

1. Go to [Cloudflare Dashboard](https://dash.cloudflare.com/)
2. Navigate to **Pages** in the left sidebar
3. Click **"Create a project"**
4. Choose **"Connect to Git"**
5. Select your Git provider (GitHub, GitLab, or Bitbucket)
6. Authorize Cloudflare to access your repositories
7. Select your `japanschoolexperience` repository

### 3. Configure Build Settings

In the Cloudflare Pages setup:

**Framework preset:** `None` (or `Eleventy` if available)

**Build command:**
```bash
npm run build
```

**Build output directory:**
```bash
dist
```

**Root directory:** (leave empty unless your project is in a subfolder)

### 4. Environment Variables

If you need any environment variables, add them in the **Environment variables** section:

- `ELEVENTY_ENV`: `production`
- `NODE_VERSION`: `20` (or latest LTS)

### 5. Deploy

1. Click **"Save and Deploy"**
2. Cloudflare will:
   - Install dependencies (`npm install`)
   - Run the build command (`npm run build`)
   - Deploy the `dist` folder to Pages

### 6. Custom Domain (Optional)

After deployment:

1. Go to your project in Cloudflare Pages
2. Click **"Custom domains"**
3. Add your domain name
4. Follow the DNS setup instructions

## Build Configuration

Your project is already configured with the correct build settings:

- **Build command:** `npm run build`
- **Output directory:** `dist`
- **Node.js version:** 20.x (as specified in package.json)

## File Structure

The following files are important for deployment:

- `package.json` - Contains build scripts and dependencies
- `eleventy.config.js` - Eleventy configuration
- `src/common/_redirects.njk` - Generates `_redirects` file for Cloudflare Pages routing
- `dist/` - Output directory (created during build)

## Troubleshooting

### Build Fails
- Check the build logs in Cloudflare Pages dashboard
- Ensure all dependencies are listed in `package.json`
- Verify Node.js version compatibility

### 404 Errors
- The `_redirects` file should handle routing
- Check that all pages have correct permalinks

### Performance
- Cloudflare Pages automatically provides CDN and optimization
- Images are optimized through Eleventy Image plugin

## Monitoring

After deployment, you can monitor:
- Build logs and deployment status
- Analytics in Cloudflare Pages dashboard
- Performance metrics
- Error tracking

## Updates

To update your site:
1. Make changes locally
2. Commit and push to your Git repository
3. Cloudflare Pages will automatically rebuild and deploy

Your site will be available at: `https://your-project-name.pages.dev`
