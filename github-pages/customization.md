---
title: GitHub Pages Customization
description: Learn how to customize your site on a GitHub repository
---

> [GitHub Pages Walkthrough](./) / Customization

---

## Website Customization

GitHub Pages uses Jekyll to build your site by default. Jekyll gives you a lot of flexibility to customize how it builds your site. If you're using other site builder besides Jekyll, then the following walthrough guide may not suits you.

Customization options can either be specified in a `_config.yml` or `_config.toml` file placed in your site’s root directory. To customize your site even more, see "[Jekyll Configuration](https://jekyllrb.com/docs/configuration/)".

> Create `_config.yml` file at the root level of your site's directory.

## Changing the title and description

By default, the title of your site is the repository name. You can change the title and description by editing the `_config.yml`.

> Edit > `_config.yml`

```yml
title: Your site's title
description: Your site's descriptions.
```

> For detailed instruction, see "[Changing the title and description](https://docs.github.com/en/pages/quickstart#changing-the-title-and-description)".

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

I'll be listing my themes too. So be sure to check out [my website](//techie-joe.github.io/).

You can also add your own theme to customize your site’s look and feel even more.  
For more information, see "[About GitHub Jekyll Themes](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll#themes)".

## Overriding theme defaults

Typically, Jekyll theme has default assets, data, layouts, includes, and stylesheets stored in folders such as `assets`, `_data`, `_layouts`, `_includes`, and `_sass`. You can override any of the defaults with your own content. To replace it, visit the theme repository you're using and understand its file structure, then make a similar file on your repository giving it the same name as the file you wish to override. Jekyll will look first to your site’s content before looking to the theme’s defaults for any requested file. With a clear understanding of the theme’s files, you can now override any theme file by creating a similarly named file in your site directory. See "[Overriding theme defaults](https://jekyllrb.com/docs/themes/#overriding-theme-defaults)".

## Using front matter

The front matter must be the first thing in the file and must take the form of valid [YAML](https://yaml.org/) set between triple-dashed lines. Any file that contains a front matter block will be processed by the builder as a special file. Here is a basic example:

```yml
---
layout: post
title: Blogging Like a Hacker
---
```

Front matter block are used to set variables and metadata. Between these triple-dashed lines, you can set predefined variables or even create custom ones of your own, such as a title and layout. You can add front matter to the top of any `.html` or `.md` file. Read more about front matter in the [Jekyll documentation](https://jekyllrb.com/docs/frontmatter)
