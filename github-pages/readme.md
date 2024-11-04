# Techie Joe's GitHub Pages Walkthrough

Learn how to create a website directly from a repository on GitHub.
---

You can see examples of sites using GitHub Pages in the [GitHub Pages examples](https://github.com/collections/github-pages-examples).

## Static site generators

GitHub Pages publishes any static files that you push to your repository. You can create your own static files or use a static site generator to build your site for you. You can also customize your own build process locally or on another server. For more information, see "Configuring a publishing source for your GitHub Pages site."

GitHub Pages will use Jekyll to build your site by default. If you want to use a static site generator other than Jekyll, write a GitHub Actions to build and publish your site, OR disable the Jekyll build process by creating an empty file called `.nojekyll` in the root of your publishing source, then build your site locally.

GitHub Pages does not support server-side languages such as PHP, Ruby, or Python.
