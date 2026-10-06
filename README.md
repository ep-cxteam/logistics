# Support pages

Simple web pages from ExperiencePoint's Support team, such as workshop prep hubs. Each folder with an `index.html` is a live page.

## Everything here is public

This repo and every page in it can be read by anyone on the internet, and GitHub keeps every old version forever. Deleting a file takes it off the live page but does not erase it from the history.

So nothing private ever goes in here. That means no names of participants, clients or colleagues, no personal emails or phone numbers, no client logos or session details that point to a client, and no spreadsheets, documents, PDFs or screenshots of inboxes, rosters or client material.

## Before every commit: the checklist

Go through these five questions every time, even for a one-word fix.

1. **Names.** Is any person's or client's name anywhere: on the page, in a file name, inside an image, or in a comment?
2. **Contact details.** Is there a personal email address or phone number?
3. **Files.** Am I uploading only `.html` pages and images? No spreadsheets, documents, PDFs, slides or zip files.
4. **Pictures.** Does any screenshot or photo show names, an inbox, a roster or client material?
5. **Front page test.** Would I be comfortable seeing this on the front page of a search engine, forever?

If every answer is clean, write a commit message that includes the word **checked**, for example `Update EC prep hub dates (checked)`. That word is your promise that you did the checklist. If you are unsure about anything, stop and ask the repo owner before you commit.

## After every commit

1. Open the **Actions** tab. Wait for the **Safety checks** run to finish.
2. If it failed, open it, read the list, and fix each item straight away. The page is already live.
3. Open the live page in a private browser window and look at it once.

## How pages are organized

- One folder per page, named in lowercase with hyphens and no spaces, for example `ec/in-person/`.
- The page is always called `index.html`. Its address is the folder's path.
- Translations go in a subfolder named with the language code, for example `ec/in-person/fr/`.
- Shared images go in `assets/`.
- There is no homepage at the root. The bare address shows a "page not found" on purpose, so nobody can browse a list of everything here.
- Every page carries this line inside `<head>`, so search engines leave it out of results:
  `<meta name="robots" content="noindex, nofollow">`

## If something private goes out

1. Delete the file, or remove the private part, and commit. That takes it off the live page within a few minutes.
2. Tell the repo owner straight away, even if you fixed it. The old version is still in the history, and the owner decides what else to do.
3. If it was a password or key of any kind, treat it as stolen and replace it.

## How it works

GitHub Pages publishes the `main` branch as it is. The empty `.nojekyll` file tells GitHub to serve files exactly as uploaded. The **Safety checks** in `.github/workflows/checks.yml` run on every change and flag anything that looks private.
