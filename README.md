# Simple Site Maintenance Page

A clean, responsive maintenance page that can be quickly deployed to Cloudflare Pages for temporary site downtime notices. Perfect for scheduled maintenance or emergency downtime situations.

![Maintenance Page Preview](https://api.placeholder.com/600/400)

## Features

- 🚀 Zero build configuration required
- 📱 Fully responsive design
- ⚡ Fast deployment through Cloudflare Pages
- 🎨 Clean, modern aesthetic
- 💨 Lightweight (single HTML file)
- 🔄 Handles all routes automatically

## Quick Start

1. Fork or clone this repository
2. Connect to Cloudflare Pages:
   ```bash
   # No build steps required!
   # Just push to your repository
   git clone https://github.com/yourusername/maintenance-page
   cd maintenance-page
   ```

## Deployment Steps

1. In your Cloudflare dashboard, go to **Pages** → **Create a project** → **Connect to Git**
2. Select your repository
3. Configure your build settings:
   - Build command: *leave empty*
   - Build output directory: `/`
4. Click "Save and Deploy"

## Redirecting Traffic

### Option 1: Using DNS
1. Go to DNS in your Cloudflare dashboard
2. Create a CNAME record:
   ```
   Type: CNAME
   Name: your-subdomain
   Target: your-project.pages.dev
   Proxy status: Proxied
   ```

### Option 2: Using Page Rules
1. Go to **Rules** → **Page Rules** in your Cloudflare dashboard
2. Create a new rule:
   ```
   URL pattern: subdomain.yourdomain.com/*
   Setting: Forward URL
   Status: 302 (Temporary Redirect)
   Destination URL: your-maintenance-page.pages.dev
   ```

## Customization

The maintenance page can be easily customized by modifying the `index.html` file:

- Change the text content
- Modify the color scheme in the `<style>` section
- Add your company logo
- Update contact information

## Files

- `index.html` - The maintenance page
- `_redirects` - Netlify/Cloudflare Pages configuration to handle all routes
- `README.md` - This documentation

## License

MIT License - Feel free to use this for your own projects.

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Support

If you encounter any issues or have questions:
1. Open an issue in this repository
2. Check [Cloudflare's documentation](https://developers.cloudflare.com/pages)