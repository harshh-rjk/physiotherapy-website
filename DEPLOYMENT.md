# Deployment Guide for Physiotherapy Website

## Option 1: GitHub Pages (Free & Easy)

### Step-by-Step:

1. **Go to Repository Settings**
   - Navigate to: https://github.com/harshh-rjk/physiotherapy-website/settings
   - Click on "Pages" in the left sidebar

2. **Enable GitHub Pages**
   - Under "Source", select: **Deploy from a branch**
   - Choose branch: **main**
   - Choose folder: **/ (root)**
   - Click **Save**

3. **Your site will be live at:**
   ```
   https://harshh-rjk.github.io/physiotherapy-website/
   ```

4. **Setup Custom Domain (Optional)**
   - Add your domain (e.g., drlalamehra.com) in the "Custom domain" field
   - Update DNS records with your domain registrar

---

## Option 2: Netlify (Recommended for Beginners)

### Benefits:
- Free SSL certificate
- Custom domain support
- Better build features
- Analytics

### Steps:

1. **Sign Up at Netlify**
   - Go to: https://app.netlify.com
   - Click "Sign up" and choose "GitHub"
   - Authorize Netlify to access your GitHub

2. **Create New Site**
   - Click "New site from Git"
   - Select your GitHub account
   - Choose "physiotherapy-website" repository

3. **Configure Build Settings**
   - Build command: Leave empty (static site)
   - Publish directory: `.` (root)
   - Click "Deploy"

4. **Your site will be at:**
   ```
   https://[random-name].netlify.app
   ```

5. **Add Custom Domain**
   - Go to Site settings → Domain management
   - Add your custom domain

---

## Option 3: Vercel (Best Performance)

### Steps:

1. **Sign Up at Vercel**
   - Go to: https://vercel.com
   - Click "Sign Up" and choose "Continue with GitHub"

2. **Import Project**
   - Click "Import Project"
   - Select "physiotherapy-website" from your GitHub

3. **Deploy**
   - Framework: Choose "Other" (static site)
   - Click "Deploy"

4. **Your site will be at:**
   ```
   https://physiotherapy-website.vercel.app
   ```

---

## Quick Comparison

| Feature | GitHub Pages | Netlify | Vercel |
|---------|------------|---------|--------|
| Cost | Free | Free | Free |
| Custom Domain | Yes | Yes | Yes |
| SSL Certificate | Yes | Yes | Yes |
| Ease of Setup | ⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ |
| Performance | Good | Excellent | Excellent |
| Support | GitHub Docs | Great Docs | Great Docs |

---

## Recommended: GitHub Pages + Cloudflare

1. Enable GitHub Pages (see Option 1)
2. Get a domain from: GoDaddy, Namecheap, or Route53
3. Set up free Cloudflare DNS for SSL and caching
4. Update nameservers to Cloudflare
5. Add DNS records pointing to GitHub Pages

---

## After Deployment

### Update Form Submission
The website currently uses Formspree. To customize:

1. Go to: https://formspree.io
2. Sign up and verify your email
3. Replace the form action URL with your Formspree endpoint:
   ```html
   action="https://formspree.io/f/YOUR_FORM_ID"
   ```

### Update Contact Links
Edit these in `index.html`:
- WhatsApp: `https://wa.me/919425675733`
- Phone numbers in header
- Email address in footer

### Track Website Analytics
Add Google Analytics:
```html
<!-- Add before </head> -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_ID');
</script>
```

---

## Troubleshooting

### GitHub Pages not showing?
- Wait 5-10 minutes after enabling
- Check repository is public
- Verify `index.html` exists in root

### Custom domain not working?
- Check DNS records are correct
- Wait for DNS propagation (up to 48 hours)
- Use https://dnschecker.org to verify

### Form not submitting?
- Verify Formspree endpoint is correct
- Check browser console for errors
- Test with sample data first

---

## Support Links
- GitHub Pages: https://docs.github.com/en/pages
- Netlify Docs: https://docs.netlify.com
- Vercel Docs: https://vercel.com/docs
- Formspree Help: https://formspree.io/help
