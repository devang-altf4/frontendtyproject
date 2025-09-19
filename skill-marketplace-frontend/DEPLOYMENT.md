# Vercel Deployment Checklist

## Pre-Deployment Checklist

- [ ] **Environment Variables**: Update `.env.example` with all required variables
- [ ] **API URLs**: Ensure `VITE_API_URL` points to your production backend
- [ ] **Build Test**: Run `npm run build` locally to ensure it builds successfully
- [ ] **Preview Test**: Run `npm run preview` to test the production build locally
- [ ] **Linting**: Run `npm run lint` to check for code issues
- [ ] **Dependencies**: Ensure all dependencies are properly listed in `package.json`

## Deployment Steps

### Method 1: Vercel CLI
1. Install Vercel CLI: `npm install -g vercel`
2. Login: `vercel login`
3. Deploy: `vercel` (from project root)
4. Follow prompts to configure

### Method 2: Git Integration
1. Push code to GitHub/GitLab/Bitbucket
2. Go to [vercel.com](https://vercel.com)
3. Import your repository
4. Configure environment variables in dashboard
5. Deploy

## Post-Deployment

- [ ] **Test Routes**: Verify all routes work correctly
- [ ] **API Connection**: Ensure frontend connects to backend API
- [ ] **Environment Variables**: Confirm all env vars are set in Vercel dashboard
- [ ] **Custom Domain**: Set up custom domain if needed
- [ ] **SSL Certificate**: Verify HTTPS is working
- [ ] **Performance**: Check Core Web Vitals in Vercel dashboard

## Environment Variables to Set in Vercel

```
VITE_API_URL=https://your-backend-api.vercel.app
```

Add any additional environment variables your app requires.

## Troubleshooting

### Common Issues:

1. **Build Fails**: Check build logs in Vercel dashboard
2. **Routes Don't Work**: Ensure `vercel.json` routing configuration is correct
3. **API Calls Fail**: Verify `VITE_API_URL` environment variable
4. **Assets Not Loading**: Check asset paths and public folder structure

### Useful Commands:

- `vercel logs` - View deployment logs
- `vercel --prod` - Deploy to production
- `vercel env` - Manage environment variables
- `vercel domains` - Manage custom domains

## Performance Optimization

The project is already optimized with:
- Code splitting for vendor and router bundles
- Minification with Terser
- Optimized asset handling
- Production environment configuration

## Monitoring

Use Vercel's dashboard to monitor:
- Build times
- Core Web Vitals
- Function logs (if using API routes)
- Traffic analytics