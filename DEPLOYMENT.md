# Deployment Guide

## GitHub Setup

### 1. Create a GitHub Repository

1. Go to [GitHub](https://github.com) and create a new repository
2. Name it `proficiency-test-system` or your preferred name
3. Don't initialize with README (we already have one)

### 2. Push to GitHub

In your local project directory, run these commands:

```bash
# Initialize git repository
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit: Proficiency Test System"

# Add your GitHub repository as origin
git remote add origin https://github.com/yourusername/proficiency-test-system.git

# Push to GitHub
git push -u origin main
```

### 3. Environment Variables

Make sure to set up your environment variables in your deployment platform:

```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

## Deployment Options

### Option 1: Netlify (Recommended)

1. Connect your GitHub repository to Netlify
2. Set build command: `npm run build`
3. Set publish directory: `dist`
4. Add environment variables in Netlify dashboard
5. Deploy!

### Option 2: Vercel

1. Connect your GitHub repository to Vercel
2. Vercel will auto-detect the Vite configuration
3. Add environment variables in Vercel dashboard
4. Deploy!

### Option 3: GitHub Pages

1. Install gh-pages: `npm install --save-dev gh-pages`
2. Add to package.json scripts:
   ```json
   "homepage": "https://yourusername.github.io/proficiency-test-system",
   "predeploy": "npm run build",
   "deploy": "gh-pages -d dist"
   ```
3. Run: `npm run deploy`

## Database Setup

Your Supabase database is already configured with all necessary migrations. Make sure to:

1. Run all migrations in your Supabase dashboard
2. Set up storage buckets for lab reports
3. Configure authentication settings
4. Set up any necessary API keys

## Post-Deployment Checklist

- [ ] Test all user roles and authentication
- [ ] Verify file upload functionality
- [ ] Test real-time notifications
- [ ] Check all dashboard features
- [ ] Verify email notifications (if configured)
- [ ] Test search functionality
- [ ] Verify responsive design on mobile devices

## Monitoring

Consider setting up:
- Error tracking (Sentry)
- Analytics (Google Analytics)
- Uptime monitoring
- Performance monitoring

## Security

- Ensure all environment variables are properly secured
- Review Supabase RLS policies
- Set up proper CORS settings
- Enable HTTPS
- Regular security updates