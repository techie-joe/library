> [GitHub Pages Walkthrough](../) / Quick start

---

## Quick start

The quickest way to set up your site on GitHub is by using a pre-made theme. You can then modify your site content and style by editing the source code.

---

## Creating a repository for your site

Before you can create your site, you must have a repository for it. Create a new one or use an existing repository.  
See "[Creating a repository for your site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-a-repository-for-your-site)."

1. On GitHub, navigate to your site's repository.
2. Under the repository, go to the repository `Settings` tab then look for `> Code and automation > Pages`. 
3. Under the `Build and deployment > Source`, select `Deploy from a branch`, then use the branch dropdown menu and select a publishing source.

Once completed, you should be able to view your new website at `[username].github.io` for the main site, or `[username].github.io/[repository-name]` for repositories. Note that it can take up to 10 minutes for changes to your site to publish after you push the changes to GitHub. You can see the deployment process in `Actions` tab.

> For detailed explanations of all the steps mentioned above, read [Quickstart for GitHub Pages](https://docs.github.com/en/pages/quickstart).

---

## Creating entry files and pages

Create the entry file for your site at the top level of the source folder. GitHub Pages will look for an `index.html`, `index.md`, or `README.md` file as the entry file for your site. You can add more pages to your site by creating more new files in `.html` or `.md`. Each file will be available on your site in the same directory structure as your publishing source.

You can create a custom 404 error page for people trying to access nonexistent pages on your site.  
See "[Creating a custom 404 page for your GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-custom-404-page-for-your-github-pages-site)".

---

## Changing the title and description

By default, the title of your site is the repository name. You can change the title and description by editing the `_config.yml` file in your repository.

> At the top level of your source folder ..  
> Edit > `_config.yml`

```yml
title: Your site's title
description: Your site's descriptions.
```

> For detailed instruction, see "[Changing the title and description](https://docs.github.com/en/pages/quickstart#changing-the-title-and-description)".

---

## Theme customizations

The quickest way to apply a theme to your site is by using `remote_theme`.

> Edit > `_config.yml`  
> Add ..

```yml
remote_theme: [theme-repository]
```
for example :
```yml
remote_theme: techie-joe/pages
```

To customize your site even more, you can use Jekyll, a static site generator with built-in support for GitHub Pages.  
For more information, see "[About GitHub Pages and Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll)".

You can also add your own theme to customize your site’s look and feel even more.  
For more information, see "[Adding a theme to your GitHub Pages site using Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-a-theme-to-your-github-pages-site-using-jekyll)".

---

## Using front matter

To set variables and metadata, such as a title and layout, for a page or post on your site, you can add YAML front matter to the top of any Markdown or HTML file. Read about front matter in the [Jekyll documentation](https://jekyllrb.com/docs/frontmatter)

## Repository metadata

You can add `site.github` to a post or page to add any repository metadata to your site.  
For more information, see "[Using site.github](https://jekyll.github.io/github-metadata/site.github/)" in the Jekyll Metadata documentation.

---

## Custom domains

GitHub Pages supports using custom domains, or changing the root of your site's URL from the default, like `[username].github.io`, to any domain you own, like `[yourdomain.com]`.

> See "[About custom domains and GitHub Pages](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages)".

---

## Securing site with HTTPS

HTTPS adds a layer of encryption that prevents others from snooping on or tampering with traffic to your site. You can enforce HTTPS for your GitHub Pages site to transparently redirect all HTTP requests to HTTPS.

> See "[Securing your GitHub Pages site with HTTPS](https://docs.github.com/en/pages/getting-started-with-github-pages/securing-your-github-pages-site-with-https)".

---

## Deleting site

> You can delete a site. See "[Deleting a GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/deleting-a-github-pages-site)".  

OR

> Unpublish it. See "[Unpublishing a GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/unpublishing-a-github-pages-site)".

---

## Troubleshooting errors

This guide will help you troubleshoot common reasons you may be seeing a 404 error.

> See "[Troubleshooting 404 errors for GitHub Pages sites](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-404-errors-for-github-pages-sites)".
