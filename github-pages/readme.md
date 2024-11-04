# Techie Joe's GitHub Pages Walkthrough

Learn how to create a website directly from a GitHub repository.
---

GitHub Pages are public webpages hosted and published through GitHub. You can use GitHub Pages to showcase some open source projects, host a blog, or even share your résumé. This guide will help get you started on creating your next website. This is Techie Joe's walkthrough over the official [GitHub Pages Documentation](https://docs.github.com/en/pages) 

## Quick start

The quickest way to get up and running is by a pre-made theme. You can then modify your site content and style by editing the source code.

This walktrough will lead you through creating a user site at `[username].github.io`.

 > Read [this guide](./quick-start/).

## Examples

You can see examples of sites using GitHub Pages in the [GitHub Pages examples](https://github.com/collections/github-pages-examples).

## Static site generators

GitHub Pages publishes any static files that you push to your repository. GitHub Pages will use Jekyll to build your site by default. If you want to use a static site generator other than Jekyll, write a GitHub Actions to build and publish your site, OR disable the Jekyll build process by creating an empty file called `.nojekyll` in the root of your publishing source, then build your site locally.

You can create your own static files or use a static site generator to build your site for you. You can also customize your own build process locally or on another server. For more information, see "[Configuring a publishing source for your GitHub Pages site.](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)"

GitHub Pages does not support server-side languages such as PHP, Ruby, or Python.

## Terms of use

Your use of GitHub Pages is subject to the [GitHub Terms of Service](https://docs.github.com/en/site-policy/github-terms/github-terms-of-service), including the restrictions on get-rich-quick schemes, sexually obscene content, and violent or threatening content or activity.

## Prohibited uses

GitHub Pages is not intended for or allowed to be used as a free web-hosting service to run your online business, e-commerce site, or any other website that is primarily directed at either facilitating commercial transactions or providing commercial software as a service (SaaS). GitHub Pages sites shouldn't be used for sensitive transactions like sending passwords or credit card numbers.

## Usage limits

GitHub Pages sites are subject to the following usage limits:

- GitHub Pages source repositories have a recommended limit of 1 GB. For more information, see "[About large files on GitHub](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github#file-and-repository-size-limitations)"

- Published GitHub Pages sites may be no larger than 1 GB.

- GitHub Pages deployments will timeout if they take longer than 10 minutes.

- GitHub Pages sites have a soft bandwidth limit of 100 GB per month.

- GitHub Pages sites have a soft limit of 10 builds per hour. This limit does not apply if you build and publish your site with a custom GitHub Actions workflow.

- In order to provide consistent quality of service for all GitHub Pages sites, rate limits may apply. These rate limits are not intended to interfere with legitimate uses of GitHub Pages. If your request triggers rate limiting, you will receive an appropriate response with an HTTP status code of `429`, along with an informative HTML body.

If your site exceeds these usage quotas, GitHub may not be able to serve your site, or you may receive a polite email from GitHub Support suggesting strategies for reducing your site's impact on GitHub servers, including putting a third-party content distribution network (CDN) in front of your site, making use of other GitHub features such as releases, or moving to a different hosting service that might better fit your needs.

## Data collection

When a GitHub Pages site is visited, the visitor's IP address is logged and stored for security purposes, regardless of whether the visitor has signed into GitHub or not. For more information about GitHub's security practices, see [GitHub Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-privacy-statement).

## Sensitive data

GitHub Pages sites are publicly available on the internet, even if the repository for the site is private. If you have sensitive data in your site's repository, you may want to remove the data before publishing.

## Getting started

This walktrough will lead you through creating a user site at `[username].github.io`.

 > Read [this guide](./quick-start/).
