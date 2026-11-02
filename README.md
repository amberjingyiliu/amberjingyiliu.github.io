# Jingyi Liu personal website

Plain HTML and CSS, with no build step. GitHub Pages serves the files as they are.

## Fill in before publishing

Everything still to fill in has a yellow highlight in the browser and a `TODO` comment in the source.
When all of these are done, no yellow is left on any page.

| What | Where |
| --- | --- |
| Bio and research interests | `index.html` |
| Google Scholar link (or delete the line) | `index.html` |
| Email (both the `mailto:` link and the text) | `index.html` |
| Office address (or delete the line) | `index.html` |
| Paper title, coauthors, status, abstract | `research/index.html` |
| Paper section heading and PDF link (optional) | `research/index.html` |
| Paper and data links | `research/index.html` |
| University, role, courses, terms | `teaching/index.html` |
| Dataset names, descriptions, links | `data/index.html` |
| CV: replace the placeholder, same file name | `files/CV_JingyiLiu.pdf` |

To list what is left, from this folder:

```bash
grep -rn "TODO" --include=index.html .
```

## Preview locally

From this folder, then open http://localhost:8321:

```bash
python3 -m http.server 8321
```

## Publish to GitHub Pages

Your address will be `https://USERNAME.github.io`, where `USERNAME` is your GitHub username.
Anything you upload is public, so fill in the placeholders first.

1. Sign in at github.com and create a new **public** repository named exactly `USERNAME.github.io`.
2. On the empty repository page, click **uploading an existing file**.
3. Open this folder in Finder, select everything inside it (not the folder itself), and drag it onto the page. Click **Commit changes**.
4. Go to **Settings → Pages**. Under "Build and deployment", set the source to **Deploy from a branch**, the branch to `main`, and the folder to `/ (root)`. Click **Save**.
5. Wait a minute or two, then open `https://USERNAME.github.io`.

To update the site later, use **Add file → Upload files** in the repository to replace the changed files.
GitHub redeploys on its own.

## Add a paper or dataset

1. Put the PDF in `files/papers/` or the data file in `files/data/`.
2. Copy the commented-out block in `research/index.html` or `data/index.html`, and point its links at your file.

Everything uploaded is public, so add only data you are allowed to share.
GitHub's website takes files up to 25 MB, and GitHub rejects anything over 100 MB. Host larger datasets on a data repository, then link to them.
