# Putting the site on GitHub Pages

## What is in this folder

The site follows the department job market website template in the format current UMD candidates use: EB Garamond throughout, site name at top left and the pages (Home, Curriculum Vitae, Research, Teaching) at top right, name heading with photo on the left and text on the right on Home, bold section headings with dark-red paper titles, status bullets, and abstracts that open with the arrow on Research, and course lists on Teaching. The CV is viewable in the browser.

- `index.html`: Home. Welcome, research summary, CV and resume links, contact.
- `cv.html`: the CV, displayed page by page in the browser, plus download buttons.
- `research.html`: job market paper, working papers, work in progress.
- `teaching.html`: instructor course and teaching assistant courses.
- `assets/site.css`: the styling for all four pages.
- `assets/fonts/`: EB Garamond, self-hosted.
- `assets/vendor/`: PDF.js, which draws the CV on the CV page in every browser, including phones.
- `.nojekyll`: tells GitHub Pages to serve the files as they are.

Already included: `assets/cv.pdf`, `assets/resume.pdf`, and the papers under `papers/`. The CV links each paper title to these addresses, so keep the file names when you replace a file:

- `papers/huang_jmp.pdf`: title page and abstract of the job market paper with "Paper available upon request" (https://wantian-huang.com/papers/huang_jmp.pdf). The full paper must not be posted because of the NielsenIQ data terms; the website itself does not link to this file
- `papers/scope_economies.pdf`: scope economies paper with Fan, Xu, and Yang
- `papers/ev_nevi.pdf`: title page and abstract of the EV charging paper; replace with the full paper when ready

The headshot is `assets/photo.jpg` (600 x 674 px, the 300 x 337 frame at double resolution). To change it, replace the file with the same name.

## Steps (no git needed, about 20 minutes)

1. Sign in to GitHub as Axias24.
2. New repository. Name it exactly `axias24.github.io`. Public. Create.
3. Add file > Upload files. Drag the four `.html` files, `.nojekyll`, and the whole `assets` folder into the upload area (dragging a folder keeps its structure). Commit changes.
   `.nojekyll` is a hidden file. On a Mac, press Cmd+Shift+. in Finder to see it; on Windows, turn on hidden items in the View menu. If it will not upload, create it in the repository instead: Add file > Create new file, name it `.nojekyll`, leave it empty, commit.
4. Settings > Pages > Build and deployment: Source "Deploy from a branch", branch `main`, folder `/ (root)`, Save. The site goes live at `https://axias24.github.io` within a few minutes.
5. Open it in an incognito window. Click through all four pages, the CV page, every PDF link, and the photo. Then open it on your phone.

## Updating

- Text: open the page's `.html` file in the repository, click the pencil icon, edit, commit. Live in about a minute.
- New CV, resume, or paper: upload the PDF again with the same file name; it replaces the old one, and the CV page shows the new version automatically.
- Footer date: each of the four pages has "Last updated" at the bottom.

## Check before it goes live

- The one-line summary under the job market paper title on the home page is my wording. Make sure it says what the paper says.
- The ECON 461 description on the teaching page is generic to the course title. Adjust it to your syllabus.
- The course numbers in the teaching table came from your ELMS list. Glance over them.

Everything else (abstract, paper descriptions, Amazon and research assistant descriptions, methods, placement directors) is taken from the current CV and resume.

## Custom domain (later)

1. Buy the domain (for example `wantianhuang.com`) at any registrar.
2. In the repository: Settings > Pages > Custom domain, enter `www.wantianhuang.com`, Save. GitHub adds a `CNAME` file to the repository.
3. At the registrar's DNS settings: a `CNAME` record for `www` pointing to `axias24.github.io`, and four `A` records for the bare domain pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`.
4. Back in Settings > Pages, tick "Enforce HTTPS" once it becomes available (can take up to a day).

## Where the link goes

The department CV keeps the Google Sites address. Put this address on the resume, on LinkedIn (Contact info > Website), in your email signature, and as a one-line link on the Google Sites home page.
