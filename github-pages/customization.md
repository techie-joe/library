---
title: GitHub Pages Customization
description: Learn how to customize your site on a GitHub repository
---

> [GitHub Pages Walkthrough](./) / Customization

---

## Website Customization

GitHub Pages uses Jekyll to build your site by default. Jekyll gives you a lot of flexibility to customize how it builds your site. If you're using other site builder besides Jekyll, then the following walkthrough guide may not suits you. You should have a repository set for your site, if you haven't, see [Create a repository for your site](https://techie-joe.github.io/library/github-pages/quick-start.html#create-a-repository-for-your-site).

Customization options can either be specified in a `_config.yml` or `_config.toml` file placed in your site’s root directory.  

> Create `_config.yml` file at the root level of your site's directory.

To customize your site even more, see [Jekyll Configuration](https://jekyllrb.com/docs/configuration/).

## Changing the title and description

By default, the title of your site is the repository name. You can change the title and description by editing the `_config.yml`.

> Edit > `_config.yml`

```yml
title: Your site's title
description: Your site's descriptions.
```

> For detailed instruction, see [Changing the title and description](https://docs.github.com/en/pages/quickstart#changing-the-title-and-description).

## Theme customizations

To apply a theme to your site, set the value of `remote_theme` OR `theme` with the `[THEME-NAME]` of your choice. Check the `_config.yml` of the theme's repository get it's name.

- Set `theme` if you want to use [Supported Theme by GitHub Pages](https://pages.github.com/themes/)
- Set `remote_theme` if you want to use any other Jekyll theme hosted on GitHub.

> Edit > `_config.yml`, set ..  

```yml
theme: jekyll-theme-minimal
```

OR

```yml
remote_theme: techie-joe/pages
```

I'll be listing my themes too. So be sure to check out [my website](//techie-joe.github.io/).

You can also add your own theme to customize your site’s look and feel even more.  
For more information, see "About GitHub Jekyll Themes](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll#themes).

## Overriding theme defaults

Typically, Jekyll theme has default assets, data, layouts, includes, and stylesheets stored in folders such as `assets`, `_data`, `_layouts`, `_includes`, and `_sass`. You can override any of the defaults with your own content. To replace it, visit the theme repository you're using and understand its file structure, then make a similar file on your repository giving it the same name as the file you wish to override. Jekyll will look first to your site’s content before looking to the theme’s defaults for any requested file. With a clear understanding of the theme’s files, you can now override any theme file by creating a similarly named file in your site directory. See [Overriding theme defaults](https://jekyllrb.com/docs/themes/#overriding-theme-defaults).

## Further reading

1. [Create a repository for your site](#create-a-repository-for-your-site).
2. [Create entry files and pages](#create-entry-files-and-pages).
