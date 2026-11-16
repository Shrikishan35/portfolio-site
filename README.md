# Shrikishan B: portfolio site

A static, single-page portfolio. No build step, no framework, no dependencies.

## What is in this folder

| Path | Purpose |
|---|---|
| `index.html` | The whole site (HTML, CSS and a small amount of JavaScript) |
| `assets/fonts/` | Self-hosted Source Serif 4 and IBM Plex Sans (woff2, latin subset) with their licences |
| `favicon.svg`, `favicon.ico`, `apple-touch-icon.png` | Favicon set |
| `og-image.png` | 1200 x 630 image shown when the link is shared |
| `vercel.json` | Security headers and cache rules |
| `robots.txt` | Allows search engines |

## Deploy to Vercel (free Hobby plan)

### Option A: Vercel CLI (fastest)

1. Install Node.js (nodejs.org), then in a terminal run `npm install -g vercel`.
2. `cd` into this folder.
3. Run `vercel login` and sign in (email, GitHub, GitLab or Bitbucket).
4. Run `vercel`. Answer the prompts:
   - Set up and deploy? **Yes**
   - Which scope? pick your personal account
   - Link to existing project? **No**
   - Project name: for example `shrikishan-b` (this becomes `shrikishan-b.vercel.app` if free)
   - Directory: `./`
   - Override settings? **No**
5. The first deployment of a new project is a production deployment. When it finishes, the CLI prints the URL.
6. For later updates, run `vercel --prod`.

### Option B: GitHub import

1. Create a new GitHub repository (private or public) and push this folder to it.
2. In the Vercel dashboard, add a new project and import that repository.
3. Leave Framework Preset as **Other** and leave build command and output directory empty.
4. Deploy. Every later push to the main branch redeploys the site.

## After deploying

- Open the **production** URL (`<project-name>.vercel.app`), not a per-deployment URL with random characters. Per-deployment URLs can be protected by Vercel's Deployment Protection.
- In the project, open Settings, then Deployment Protection. Make sure the production domain is not set to be protected (do not choose "All Deployments").
- Test in a private/incognito window: page loads, and the email, LinkedIn, ORCID and certificate links open.
- Optional: once you know the final URL, add absolute `og:image`, `twitter:image` and canonical tags in `index.html` so every social network shows the preview image.

## Updating content later

Edit `index.html`, save, and redeploy (`vercel --prod`, or push to GitHub). The site has a résumé download link pointing to `assets/resume.pdf`. Add the final PDF at that path when it is ready; the link is present but the file is not included yet.
