# Resume site

Plain HTML/CSS, no build step. Hosted on AWS Amplify Hosting.

## Files
- `index.html` - all the content. Edit text here.
- `styles.css` - look and feel (light/dark mode and print styles included).
- `assets/Davis-Hochstatter-Resume.pdf` - the download link target. Replace the file, keep the name.
- `amplify.yml` - tells Amplify to publish the folder as-is.

## Preview locally
```
npx serve .
```
or just open `index.html` in a browser.

## Deploy (one-time setup)
1. Push this folder to a GitHub repo (repo root = this folder).
2. AWS Console > Amplify > Create new app > GitHub > pick the repo and branch `main`.
   Accept the detected settings (it picks up `amplify.yml`).
3. After the first deploy: App settings > Domain management > Add domain.
   Choose your Route 53 domain. Amplify creates the certificate and DNS records for you.
   Add both the apex (`example.com`) and `www`, with one redirecting to the other.

## Updating
Edit, commit, push to `main`. Amplify redeploys in about a minute.
