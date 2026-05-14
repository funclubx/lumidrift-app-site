# LumiDrift Official Website

This is the static official website for the iOS app LumiDrift, operated by Guangzhou Leqi Trading Co., Ltd.

The site is built with plain HTML and CSS. It does not use a backend, database, cookies, analytics SDKs, advertising SDKs, or third-party tracking scripts.

## Pages

- `/` - Home
- `/privacy/` - Privacy Policy
- `/support/` - Support
- `/about/` - About
- `/404.html` - Not found page

## Project Structure

```text
.
├── 404.html
├── CNAME
├── README.md
├── about/
│   └── index.html
├── assets/
│   └── css/
│       └── style.css
├── index.html
├── privacy/
│   └── index.html
└── support/
    └── index.html
```

## Local Preview

For the closest preview to GitHub Pages, run a local static server from the project root:

```bash
python3 -m http.server 4173
```

Then open:

```text
http://127.0.0.1:4173/
```

You can also open `index.html` directly in a browser; the site uses relative asset paths so the CSS will still load. When previewing with `file://`, open page files such as `about/index.html` directly instead of opening the folder path `about/`.

## Deploy to GitHub Pages

1. Create a GitHub repository for this site.
2. Push these files to the repository.
3. In the repository, open **Settings → Pages**.
4. Set the source branch, usually `main`, and the folder to `/root`.
5. Set the custom domain to:

```text
lumidrift.app
```

6. Enable **Enforce HTTPS** after GitHub finishes checking the domain.

The `CNAME` file is already included and contains:

```text
lumidrift.app
```

## GoDaddy DNS Notes

After the GitHub Pages site is created, configure DNS in GoDaddy:

- For the apex/root domain `lumidrift.app`, add GitHub Pages `A` records:

```text
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

- For `www.lumidrift.app`, add a `CNAME` record pointing to the GitHub Pages default domain:

```text
<github-username>.github.io
```

Replace `<github-username>` with the GitHub account or organization name that owns the repository.

After DNS propagation, confirm these URLs are available over HTTPS:

- `https://lumidrift.app/`
- `https://lumidrift.app/privacy/`
- `https://lumidrift.app/support/`
- `https://lumidrift.app/about/`
