---
title: GitHub Pages Quick Start
description: The quickest way to set up your site on GitHub is by using a pre-made theme.
---

> [GitHub Pages Walkthrough](./) / Quick start

---

## Quick start

The quickest way to set up your site on GitHub is by using a pre-made theme. You can then modify your site content and style by editing the source code.

1. [Create a repository for your site](#create-a-repository-for-your-site).
2. [Create entry files and pages](#create-entry-files-and-pages).
3. [Customize your site](./customization.md).

## Create a repository for your site

Before you can create your site, you must have a repository for it. Create a new one or use an existing repository.  
See "[Creating a repository for your site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-a-repository-for-your-site)."

1. On GitHub, navigate to your site's repository.
2. Under the repository, go to the repository `Settings` tab then look for `> Code and automation > Pages`. 
3. Under the `Build and deployment > Source`, select `Deploy from a branch`, then use the branch dropdown menu and select a publishing source.

Once completed, you should be able to view your new website at `[username].github.io` for the main site, or `[username].github.io/[repository-name]` for repositories. Note that it can take up to 10 minutes for changes to your site to publish after you push the changes to GitHub. You can see the deployment process in `Actions` tab.

> For detailed explanations of all the steps mentioned above, read [Quickstart for GitHub Pages](https://docs.github.com/en/pages/quickstart).

## Create entry files and pages

Create the entry file for your site at the top level of the source folder. GitHub Pages will look for an `index.html`, `index.md`, or `README.md` file as the entry file for your site. You can add more pages to your site by creating more new files in `.html` or `.md`. Each file will be available on your site in the same directory structure as your publishing source.

You can add a new **page or post** to your site on GitHub Pages.  
See "[Adding content to your GitHub Pages site using Jekyll
](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-content-to-your-github-pages-site-using-jekyll)"

You can create a **custom 404 error page** for people trying to access nonexistent pages on your site.  
See "[Creating a custom 404 page for your GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-custom-404-page-for-your-github-pages-site)".

Familiarize on the basics of [front matter](https://jekyllrb.com/docs/frontmatter/), [writing posts](https://jekyllrb.com/docs/posts/), and [creating pages](https://jekyllrb.com/docs/pages/). On every content you create, start with the following **front matter**. If you don’t specify the value, default is used.

```md
---
layout: layout-name
title: "Title of the article"
description: "Short description for the article."
permalink: #optional
---
```

## Writing contents

Besides HTML, you can use Markdown to write your site contents. Markdown is a lightweight and easy-to-use syntax for styling your content. These are few commonly used syntax ..

```md
# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` ~~Strikethrough~~

[Link](url) and ![Image](src)

`inline code`
> block quote

```

> Read [Getting started with writing and formatting on GitHub](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github)

## Using front matter

The front matter must be the first thing in the file and must take the form of valid [YAML](https://yaml.org/) set between triple-dashed lines. Any file that contains a front matter block will be processed by the builder as a special file. Here is a basic example:

```yml
---
layout: post
title: Blogging Like a Hacker
---
```

Front matter block are used to set variables and metadata. Between these triple-dashed lines, you can set predefined variables or even create custom ones of your own, such as a title and layout. You can add front matter to the top of any `.html` or `.md` file. Read more about front matter in the [Jekyll documentation](https://jekyllrb.com/docs/frontmatter)

## Metadata variables

Metadata variables such as `site`, `layout`, and `page`, is accessible to your site by referencing it using moustache `{% raw %} {{ [variable-namespace] }} {% endraw %}`.  
Example:  
```md
{% raw %}{{ site.title }}
{{ page.description }}{% endraw %}
```

Repository metadata variables is exposed to your site in the `site.github` namespace.
For more information, see "[Using site.github](https://jekyll.github.io/github-metadata/site.github/)".

## Customize your site

GitHub Pages uses Jekyll to build your site by default. Jekyll gives you a lot of flexibility to customize how it builds your site. If you're using other site builder besides Jekyll, then the following walthrough guide may not suits you.

> To customize your site, see [Website Customization](./customization.md)

## Custom domains

GitHub Pages supports using custom domains, or changing the root of your site's URL from the default, like `[username].github.io`, to any domain you own, like `[yourdomain.com]`.

> See "[About custom domains and GitHub Pages](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages)".

## Securing site with HTTPS

HTTPS adds a layer of encryption that prevents others from snooping on or tampering with traffic to your site. You can enforce HTTPS for your GitHub Pages site to transparently redirect all HTTP requests to HTTPS.

> See "[Securing your GitHub Pages site with HTTPS](https://docs.github.com/en/pages/getting-started-with-github-pages/securing-your-github-pages-site-with-https)".

## Deleting site

> You can delete a site. See "[Deleting a GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/deleting-a-github-pages-site)".  

OR

> Unpublish it. See "[Unpublishing a GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/unpublishing-a-github-pages-site)".

## Troubleshooting errors

This guide will help you troubleshoot common reasons you may be seeing a 404 error.

> See "[Troubleshooting 404 errors for GitHub Pages sites](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-404-errors-for-github-pages-sites)".

## Further reading

> To customize your site, see [Website Customization](./customization.md)
