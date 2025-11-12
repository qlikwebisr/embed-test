# Qlik Embed Simple Example

A simple web application demonstrating how to embed Qlik Sense visualizations using the Qlik Embed Web Components library with OAuth2 authentication.

## Technologies

- HTML/CSS/JavaScript
- Qlik Embed Web Components
- OAuth2 Authentication
- Nginx (for Railway deployment)

## Deployment on Railway

This app is configured to deploy on Railway with proper CSP headers for Qlik Embed.

### Configuration Files:
- `nginx.conf` - Nginx server configuration with CSP headers including 'unsafe-eval'
- `nixpacks.toml` - Nixpacks build configuration
- `railway.toml` - Railway deployment configuration

### Important Notes:
1. The CSP headers are set at the **nginx server level** (not in HTML meta tags) to ensure they are properly applied
2. Railway will automatically detect `nixpacks.toml` and use nginx
3. Make sure your Qlik OAuth client is configured with the Railway URL: `https://embed-test-production.up.railway.app`
4. After deployment, do a hard refresh (Ctrl+Shift+R) to clear browser cache

### Deployment Steps:
1. Commit all changes to git
2. Push to GitHub: `git push origin main`
3. Railway will automatically detect and deploy
4. Wait for deployment to complete
5. Test the app with a hard refresh

## Documentation Links

- [Qlik Embed Documentation](https://qlik.dev/embed/qlik-embed/)
- [OAuth Configuration Example](https://qlik.dev/examples/qlik-embed-examples/oauth-config-example/)
- [Quickstart Web Component Guide](https://qlik.dev/examples/qlik-embed-examples/quickstart-webcomponent-complete/)


