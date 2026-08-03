# Whisked & Away — Setup Guide 🍵

Your blog with a built-in editor. One-time setup (~20 min), then publishing a post takes 2 minutes from any browser.

## One-time setup

### 1. Put the site on GitHub
1. Create a free account at github.com
2. Click **+ → New repository**, name it `whisked-away-site`, keep it **Public**, click Create
3. Click **uploading an existing file**, drag ALL the files/folders from this folder in (everything: admin, css, images, posts, _includes, index.njk, package.json, netlify.toml, eleventy.config.js, README.md)
4. Click **Commit changes**

### 2. Put the site live on Netlify
1. Sign up at netlify.com — choose **Sign up with GitHub**
2. Click **Add new site → Import an existing project → GitHub**, pick `whisked-away-site`
3. Click **Deploy** (settings are auto-detected). In ~1 minute your site is live at `something.netlify.app`
4. Optional: rename it (Site configuration → Change site name) or connect your own domain (Domain management)

### 3. Switch on the editor login
1. On GitHub, open `admin/config.yml`, click the pencil ✏️, replace `YOUR-GITHUB-USERNAME` with your GitHub username, commit
2. Create the login key: go to github.com/settings/developers → **OAuth Apps → New OAuth App**
   - Application name: `Whisked Away CMS`
   - Homepage URL: `https://app.netlify.com`
   - Authorization callback URL: `https://api.netlify.com/auth/done`
   - Click Register, then **Generate a new client secret**. Keep this page open.
3. In Netlify: **Site configuration → Access & security → OAuth → Install provider → GitHub**, paste the Client ID and Client Secret from step 2

## Writing posts (every time)

1. Go to `yoursite.netlify.app/admin`
2. Log in with GitHub (first time only)
3. Click **New Blog Posts** → write your post, upload a cover image, pick a category
4. Click **Publish**. The site rebuilds itself — live in about a minute. That's it!

The sample posts are in the editor too — open them and replace with your real writing, or delete them.

## Tips
- Images: upload right inside the editor (they land in images/uploads)
- Want design changes, new sections, or new categories? Ask Claude — describe the change and paste back the updated files, or connect this folder in Cowork
