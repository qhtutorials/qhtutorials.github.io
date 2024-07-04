---
title: "How to Set Up a Hugo Blog"
date: 2024-09-13T02:01:58+05:30
description: "Want to start a blog quickly? This post covers how to set up a Hugo blog on GitHub pages."
tags: [Hugo]
---
This tutorial covers:

## 1. [What is Hugo?](#1)

## 2. [Installation Requirements](#2)

## 3. [How to Set Up a Hugo Blog on GitHub Pages](#3)

<br />

<h1 id="1">What is Hugo?</h1>

Hugo is one of the fastest static site generators (SSG) that uses the Go language to create websites. For example, technical writing portfolio blogs made with Hugo can be deployed on GitHub Pages or Netlify. Because the official Hugo documentation is too long and technical for beginners, this post aims to provide a quick start guide on how to set up a Hugo blog using the Archie theme. 

<h1 id="2">Installation Requirements</h1>

Before setting up a Hugo blog, please install the following:

* Git
* Go
* PowerShell (NOT Windows PowerShell)
* Visual Studio Code

<h1 id="3">How to Set Up a Hugo Blog on GitHub Pages</h1>

-Step 1: Open PowerShell. Create and navigate to the directory that will hold your Hugo blog site:

```sh
mkdir yourfoldername
cd yourfoldername
```

-Step 2: Run this Hugo command to create a new Hugo site:

```sh
hugo new site yoursitename
```

Note: If you are deploying on GitHub pages, your site name must be your **GitHubUsername.github.io**. For example, my GitHub username is 'qhtutorials' and my blog site is 'qhtutorials.github.io'.

-Step 3: Navigate into the themes folder of your Hugo site folder:

```sh
cd yoursitename
cd themes
```

-Step 4: Add the "Archie" theme to your Hugo site by running:

```sh
git init
git submodule add https://github.com/athul/archie.git
git submodule update --remote
```

Note: Complete this step to avoid the GitHub Pages error of "no URL found for submodule path".

-Step 5: In the root of your site folder, open the hugo.toml file (in an editor such as Visual Studio Code). Edit the following:

```
baseURL = "https://YourGitHubUsername.github.io/"
title = "yoursitename"
theme = "archie"
```

-Step 6: Open the themes folder of your site and then open the Archie folder. Copy and paste the Archie layout, assets, static, and content folders into your corresponding site folders. Use this Hugo command to run the site locally:

```sh
hugo server
```

-Step 7: Add this line to the front matter in the hugo.toml file:

```
publishDir = "docs"
```

Then publish the site with:

```sh
hugo
```

-Step 8: In Visual Studio Code, create an empty .nojekyll file and save it in the docs folder in the root of your site. 

-Step 9: Log into your GitHub account and create a new repository called "yoursitename". Copy the URL of this repository.

-Step 10: On your local machine, run:

```sh
git remote set-url origin yourrepourl
```

or

```sh
git remote add origin yourrepourl
```

Check the status of your remotes with:

```sh
git remote -v
```

It should say: 

```
origin yourrepourl (fetch)
origin yourrepourl (push)
```

-Step 11: In GitHub, click your site repository and click the "Settings" button. In the left menu click "Pages" and under the "Source" drop-down menu, click "Deploy from a branch". Change the branch from "master" to "docs".

-Step 12: On your local machine, push to GitHub:

```sh
git push origin master
```

-Step 13: In GitHub, click "Actions". After your site builds and deploys, click the URL to view it.

-Step 14: To deploy on GitHub using GitHub Actions, first go to your local machine and first create a .github/workflows/hugo.yaml file in the root of your site. Paste the long yaml code from the [Hugo quick start guide](https://gohugo.io/hosting-and-deployment/hosting-on-github/) into your hugo.yaml file. Make sure to replace the "main" branch with "master" and the "publish" directory to "docs".

-Step 15: On GitHub, go back to your site GitHub Pages settings and click the "Source" drop-down menu to select "GitHub Actions". After the site builds and deployes, click the URL to view it.

Your Hugo blog is now set up on GitHub Pages. In the next post, learn how to create your first blog post.

<br />



