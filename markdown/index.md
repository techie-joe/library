# Markdown Syntax
###### Tips and tricks on mastering markdown syntaxes

Markdown is a light-weight markup language with plain text formatting syntax. It's often used to format readme files, for writing messages in online discussion forums, and to create rich text using a plain text editor.

Here are some key elements of Markdown syntax:

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

> Block quote

`Inline code`

```

> Read [Getting started with writing and formatting on GitHub](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github)

## Code blocks

Code blocks can be used to display your codes on your website. Use triple backticks <code>\`\`\`</code> to form a code block, then close it with another triple backticks <code>\`\`\`</code>. Anyting in between will be written in code blocks.

````
```
Code blocks
```
````

### Syntax highlighting for code blocks

You can also apply syntax highlighting to code blocks by specifying it's language right after the opening backticks <code>```language</code>. See "[Creating and highlighting code blocks](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks)."

##### For example

````html
```html
  <html>
    <title>Html code blocks</title>
    <body>Will format and render html codes</body>
  </html>
```
````

The supported languages for syntax highlighting depends on the builder you use.

**GitHub Pages** use [Linguist][liguist] to perform language detection and syntax highlighting. You can find out which keywords are valid in [the languages YAML file][yamllang]. See the `aliases` attibutes.

[liguist]: https://github.com/github-linguist/linguist
[yamllang]: https://github.com/github-linguist/linguist/blob/master/lib/linguist/languages.yml

##### For example
```yml
ApacheConf:
  aliases:
  - aconf
  - apache
```

````apache
```apache
<IfModule mod_rewrite.c>

# Turn on engine
RewriteEngine On

# return 301 for old-page to new-page
RewriteRule ^old-page$ /new-page [R=301,L]

</IfModule>
```
````

**Bitbucket** has it's own support list [Bitbucket markdown supported languages](https://bitbucket.org/tutorials/markdowndemo/src/master/#markdown-header-code-and-syntax-highlighting).

&nbsp;  