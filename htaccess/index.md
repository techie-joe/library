# Using .htaccess

`.htaccess` file is a configuration file used by the **Apache Web Server** to manage server settings on a per-directory basis. The name **htaccess** stands for "hypertext access," and it allows you to control the behavior of your website without modifying the main server configuration files. This article explains how you can use `.htaccess` file in your website.

## Options directive

The **Options** directive is both complicated and important. Please see [Options Directive](http://httpd.apache.org/docs/2.4/mod/core.html#options) for more information.

#### Example

This simple line of code will prevent users from seeing the contents of directories without an index file.

> Edit `.htaccess`

```apache

# This simple line of code will prevent users from seeing
# the contents of directories without an index file.
Options -Indexes

#
# Possible values for the Options directive are "None", "All",
# or any combination of:
#   Options None
#   Options All
#   Options Indexes Includes FollowSymLinks SymLinksifOwnerMatch ExecCGI MultiViews
#

```

## RewriteEngine

The `RewriteEngine` directive used in Apache's `mod_rewrite` module allows you to rewrite URLs on your server, which can be useful for a variety of tasks such as:

- **Improving SEO**: By making URLs more readable and keyword-friendly.
- **Redirecting URLs**: Sending traffic from an old URL to a new one.
- **Access Control**: Blocking certain requests based on their patterns.
- **URL Simplification**: Converting complex query strings into cleaner, more user-friendly URLs.

When you turn on the `RewriteEngine` in your `.htaccess` file, you can start using rewrite rules to transform incoming requests.

#### Example

This rule redirect requests from `old-page` to `new-page` with a **301 (permanent) redirect**

> Edit `.htaccess`
```apache
<IfModule mod_rewrite.c>

# Turn on engine
RewriteEngine On

# return 301 for old-page to new-page
RewriteRule ^old-page$ /new-page [R=301,L]

</IfModule>
```

`mod_rewrite`: is the name of the Apache module used for URL rewriting; to check if the mod_rewrite module is enabled before executing the enclosed directives.

`mod_rewrite.c`: specifically refers to the C source file that implements the mod_rewrite module in Apache; a conditional context to check the presence of the mod_rewrite module in Apache configuration, whether mod_rewrite module is loaded and available. It is more of a technical reference to the underlying implementation file of the mod_rewrite module.

`RewriteEngine On`: enables the rewrite engine.

#### RewriteRule

`RewriteRule`: uses regular expressions to match URL patterns.

`RewriteRule ^ -`: `^` matches any URL, then `-` does not rewrite it.

`RewriteRule .`: will match any URL that contains at least one character.

`RewriteRule ^`: will match any URL including an empty string.

`R=404`: returns a 404 error not found.

`R=301`: redirect request with a 301 (permanent) redirect.

The `L` flag indicates that this is the last rule to be processed.

#### RewriteCond

This examples shows few other conditions to use with `RewriteCond`.

> Edit `.htaccess`
```apache
<IfModule mod_rewrite.c>

# Turn on engine
RewriteEngine On

# This rule return 404 on all request for forbidden directory
RewriteCond %{REQUEST_URI} ^/forbidden/ [NC]
RewriteRule ^ - [R=404,L]

# This rule return 404 if the requested resource is not an existing file.
RewriteCond %{REQUEST_FILENAME} !-f
RewriteRule ^ - [R=404,L]

# This rule redirects to index.php if the requested resource is not an existing directory.
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule ^ /index.php

# This rule redirects all requests to index.php
RewriteRule ^ /index.php

# This rule return 404 on all request
RewriteRule ^ - [R=404,L]

</IfModule>
```

`RewriteCond %{REQUEST_URI} ^/forbidden/`: will match all request for forbidden directory.

`[NC]`: is a flag for (case-insensitive).

`RewriteCond %{REQUEST_FILENAME} !-f`: checks if the requested resource is not an existing file.

`RewriteCond %{REQUEST_FILENAME} !-d`: checks if the requested resource is not an existing directory.

&nbsp;
