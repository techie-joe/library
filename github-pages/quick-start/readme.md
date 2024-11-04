> [GitHub Pages Walkthrough](../) / Qucik start

---

## Quick start

The quickest way to set up your site is by using a pre-made theme. You can then modify your site content and style by editing the source code. This guide will lead you through creating a user site at `[username].github.io`.

---

## Creating site's repository

Before you can create your site, you must have a repository for your site on GitHub. Create a new one or use an existing repository. See "[Creating a repository for your site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-a-repository-for-your-site)."

1. On GitHub, navigate to your site's repository.
2. Under the repository, go to repository `Settings > Code and automation > Pages`. If you cannot see the "Settings" tab, select the  dropdown menu, then click Settings.
3. Under `Build and deployment > Source`, select `Deploy from a branch`, then use the branch dropdown menu and select a publishing source.

Once completed, you should be able to visit `[username].github.io` to view your new website. Note that it can take up to 10 minutes for changes to your site to publish after you push the changes to GitHub. You can see the deployment process in `Actions` tab.

> All the above steps are explained in [Quickstart for GitHub Pages](https://docs.github.com/en/pages/quickstart).

---

## Changing the title and description

By default, the title of your site is the repository name. You can change the title and description by editing the `_config.yml` file in your repository.

> Edit > `_config.yml`

```yml
title: Your site's title
description: Your site's descriptions.
```

> See [this guide](https://docs.github.com/en/pages/quickstart#changing-the-title-and-description)

---

## Creating entry files

Create the entry file for your site at the top level of the source folder. GitHub Pages will look for an `index.html`, `index.md`, or `README.md` file as the entry file for your site.

---

## Creating pages

You can add more pages to your site by creating more new files in `.html` or `.md`. Each file will be available on your site in the same directory structure as your publishing source.

You can display a custom 404 error page when people try to access nonexistent pages on your site. See [this guide](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-custom-404-page-for-your-github-pages-site).

---

## Customizations

The quickest way to apply a theme to your site is by using `remote_theme`.

> Edit > `_config.yml`

```yml
remote_theme: nikahmadz/pages
```

To customize your site even more, you can use Jekyll, a static site generator with built-in support for GitHub Pages. For more information, see "[About GitHub Pages and Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll)".

You can also add a theme to customize your site’s look and feel. For more information, see "[Adding a theme to your GitHub Pages site using Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-a-theme-to-your-github-pages-site-using-jekyll)".

---

## Securing site with HTTPS

HTTPS adds a layer of encryption that prevents others from snooping on or tampering with traffic to your site. You can enforce HTTPS for your GitHub Pages site to transparently redirect all HTTP requests to HTTPS.

> See [this guide](https://docs.github.com/en/pages/getting-started-with-github-pages/securing-your-github-pages-site-with-https)

---

## Custom domains

GitHub Pages supports using custom domains, or changing the root of your site's URL from the default, like `[username].github.io`, to any domain you own, like `[yourdomain.com]`.

> See [this guide](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages).

---

## Deleting site

> You can delete a site. See [this guide](https://docs.github.com/en/pages/getting-started-with-github-pages/deleting-a-github-pages-site).  

OR

> Unpublish it. See [this guide](https://docs.github.com/en/pages/getting-started-with-github-pages/unpublishing-a-github-pages-site).

---

## Troubleshooting errors

> See [this guide](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-404-errors-for-github-pages-sites).

---

## Further reading

> Read about front matter in the [Jekyll documentation](https://jekyllrb.com/docs/frontmatter)
