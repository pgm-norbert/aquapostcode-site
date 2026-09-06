# AquaPostcode public pages

Two pages Apple requires for App Store review:

- `index.html` — Support URL
- `privacy.html` — Privacy Policy URL

## Publish free on GitHub Pages

```bash
cd site
git init && git add . && git commit -m "AquaPostcode support and privacy pages"
gh repo create aquapostcode-site --public --source=. --push
gh api -X POST repos/:owner/aquapostcode-site/pages -f source[branch]=main -f source[path]=/
```

The URLs then are:

- Support:  https://<your-github-username>.github.io/aquapostcode-site/
- Privacy:  https://<your-github-username>.github.io/aquapostcode-site/privacy.html

Give both to Claude and they get written into App Store Connect.
