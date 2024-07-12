---
title: Setup Chirpy for GitHub Pages
date: 2024-07-09 16:46:00 +0800
categories: [Tools]
tags: [github, tools, jekyll]
description: Steps I followed to setup the Chirpy Jekyll theme in GitHub Pages.
---

1. Create the site from [Chirpy Starter](https://github.com/cotes2020/chirpy-starter)
   1. Sign in to GitHub
   2. Browse to [Chirpy Starter](https://github.com/cotes2020/chirpy-starter)
   3. Click the button <kbd>Use this template</kbd> &gt; <kbd>Create new repository</kbd>
   4. Name the repository `USERNAME.github.io`, where `USERNAME` is your GitHub username.
2. Go to the repository `https://github.com/USERNAME/USERNAME.github.io` and setup the deploy actions.
   1. Select *Settings* tab, then click *Pages* in the left navigation bar.
   2. In the **Source** section, select `GitHub Actions` from the dropdown menu.
   After this, the site will be built and deployed when you push to the main branch.
3. Clone the repository to your local disk, update `_config.yml` as needed.
4. Follow [Customize the Favicon](https://chirpy.cotes.page/posts/customize-the-favicon/) to update the favicons.
5. Commit and push to the remote repository
6. Check the *Actions* tab in the repository site. When the build and deploy actions complete, visit `https://USERNAME.github.io`.
