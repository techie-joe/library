# Using .htaccess

`.htaccess` file is a configuration file used by the **Apache Web Server** to manage server settings on a per-directory basis. The name .htaccess stands for "hypertext access," and it allows you to control the behavior of your website without modifying the main server configuration files. This article explains how you can use `.htaccess` file in your website.

## Example

```
<IfModule mod_rewrite.c>

# Turn on engine
RewriteEngine On

# This rule return 404 on all request for forbidden directory
RewriteCond %{REQUEST_URI} ^/forbidden/ [NC]
RewriteRule ^ - [R=404,L]

# This rule redirects all requests to index.php
RewriteRule ^ /index.php

# This rule return 404 on all request
RewriteRule ^ - [R=404,L]

</IfModule>
```

## Explanation

#### mod_rewrite

`mod_rewrite`: is the name of the Apache module used for URL rewriting; to check if the mod_rewrite module is enabled before executing the enclosed directives.

`mod_rewrite.c`: specifically refers to the C source file that implements the mod_rewrite module in Apache; a conditional context to check the presence of the mod_rewrite module in Apache configuration, whether mod_rewrite module is loaded and available. It is more of a technical reference to the underlying implementation file of the mod_rewrite module.

#### RewriteEngine

`RewriteEngine On`: enables the rewrite engine.

#### RewriteCond

`RewriteCond %{REQUEST_URI} ^/forbidden/ [NC]`: return 404 on all request for forbidden directory.

`^/forbidden/ [NC]`: is a condition statement to check if the requested URL starts with `/forbidden/` (case-insensitive due to the `[NC]` flag).

#### RewriteRule

`RewriteRule`: uses regular expressions to match URL patterns.

`RewriteRule ^ -`: matches any URL (`^`), then does not rewrite it (`-`).

`RewriteRule .`: will match any URL that contains at least one character. If you want to catch all requests, use `^`.

`RewriteRule ^`: will match any URL including an empty string. If you only want to catch requests with content, use `.`.

`[R=404,L]`: returns a 404 error (`R=404`). The `L` flag indicates that this is the last rule to be processed.

