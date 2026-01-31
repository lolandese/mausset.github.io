# Netlify Setup Guide for mausset.github.io

## Prerequisites
- GitHub account: lolandese
- Repository: https://github.com/lolandese/mausset.github.io
- Custom domain: mausset.valpellice.site
- Netlify account (already created)

## Step 1: Deploy to Netlify

1. Log into your Netlify account at https://app.netlify.com/
2. Click "Add new site" → "Import an existing project"
3. Choose "GitHub" as the Git provider
4. Select the repository: `lolandese/mausset.github.io`
5. Configure build settings:
   - **Branch to deploy**: `main`
   - **Build command**: `bundle exec jekyll build`
   - **Publish directory**: `_site`
   
   (These should be automatically detected from netlify.toml)

6. Click "Deploy site"

## Step 2: Configure Custom Domain

1. In Netlify, go to "Site settings" → "Domain management"
2. Click "Add custom domain"
3. Enter: `mausset.valpellice.site`
4. Netlify will provide DNS records to configure

### Update DNS Settings

You'll need to update your domain's DNS settings with these records:

**For subdomain (mausset.valpellice.site):**
- Type: `CNAME`
- Name: `mausset`
- Value: `<your-netlify-site-name>.netlify.app`

OR

**For apex domain (if using valpellice.site):**
- Type: `A`
- Name: `@`
- Value: Netlify's Load Balancer IP (provided in Netlify dashboard)

5. Wait for DNS propagation (can take up to 24 hours, usually faster)
6. Netlify will automatically provision an SSL certificate

## Step 3: GitHub Disable Pages (Optional)

Since you're migrating from GitHub Pages to Netlify:

1. Go to your GitHub repository settings
2. Navigate to "Pages" section
3. Under "Source", select "None" to disable GitHub Pages
4. This prevents conflicts between GitHub Pages and Netlify

## Step 4: Configure Sveltia CMS Authentication

You'll use Personal Access Token authentication for content managers.

### Generate a Personal Access Token:

1. Go to GitHub Settings → Developer settings → Personal access tokens → Tokens (classic)
2. Click "Generate new token (classic)"
3. Set the following:
   - **Note**: `Sveltia CMS - Mausset`
   - **Expiration**: Choose appropriate duration (90 days, 1 year, or no expiration)
   - **Scopes**: Check `repo` (Full control of private repositories)
     - This includes: `repo:status`, `repo_deployment`, `public_repo`, `repo:invite`
     - Also check: `Contents` (Read and write)
4. Click "Generate token"
5. **IMPORTANT**: Copy the token immediately - you won't be able to see it again!

### Access the CMS:

1. Navigate to: `https://mausset.valpellice.site/admin/`
2. Click "Sign in with Personal Access Token"
3. Paste your GitHub Personal Access Token
4. You can now manage content!

## Step 5: Test the CMS

1. Go to `https://mausset.valpellice.site/admin/`
2. Sign in with your Personal Access Token
3. Try editing a page in Italian, English, German, or French
4. Click "Publish" to commit changes to GitHub
5. Netlify will automatically rebuild and deploy the site
6. Check the "View on Live Site" button works

## Sharing Access with Content Managers

To give content managers access without GitHub accounts:

1. Generate a Personal Access Token following Step 4
2. Send them:
   - The CMS URL: `https://mausset.valpellice.site/admin/`
   - The Personal Access Token (securely - use password manager or encrypted email)
   - Instructions to click "Sign in with Personal Access Token"

**Important**: Each token provides full access to edit the site. Treat tokens as passwords.

## Troubleshooting

### Site not building?
- Check Netlify deploy logs at: Site overview → Deploys
- Common issues:
  - Missing Ruby gems: Netlify will install them automatically
  - Build timeout: Check netlify.toml configuration

### CMS not loading?
- Verify files exist:
  - `/admin/config.yml`
  - `/admin/index.html`
- Check browser console for errors

### Authentication failing?
- Verify Personal Access Token has `repo` scope with write access
- Check token hasn't expired
- Ensure repository name in admin/config.yml is correct: `lolandese/mausset.github.io`

### Changes not appearing?
- Check Netlify deploy was triggered (GitHub commit → Netlify build → Deploy)
- View deploy logs to see if build succeeded
- Try clearing browser cache

## Multi-language Structure

The CMS is configured to manage content in 4 languages:

- **Italian (IT)**: Root directory pages (index.md, about.md, etc.)
- **English (EN)**: `/en/` directory
- **German (DE)**: `/de/` directory
- **French (FR)**: `/fr/` directory

Each language has separate collections in the CMS for easy management.

## Support

- Netlify Docs: https://docs.netlify.com/
- Sveltia CMS: https://github.com/sveltia/sveltia-cms
- Jekyll Docs: https://jekyllrb.com/docs/

---

**Setup completed on**: January 31, 2026
**Repository**: https://github.com/lolandese/mausset.github.io
**Live site**: https://mausset.valpellice.site
**CMS**: https://mausset.valpellice.site/admin/
