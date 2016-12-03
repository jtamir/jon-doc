## jon-doc

Yet another static website generator, inspired by [jem-press][jem-press], [jemdoc][jemdoc], and [jemdoc+Mathjax][jemdoc-mj]. You're probably better off using one of those...

This basically supports nothing except static webpages for now, using pandocs and a simple makefile. In the future I might want to add support for Mathjax.

I used this to build my website: [jtsense.com][jtsense]

### Dependencies
Requires [Pandoc][pandoc].
Mac: 
```bash
port install pandoc
```
Linux:
```bash
apt-get install pandoc
```

### Usage:
Put Markdown files under the `content/` directory. Files in the directory with the extension `.md` will get parsed and converted to `.html`.

The navigation menu is controlled through `helper/menu.md`.

### Build and Deploy
To deploy to a server, change the variable `DEPLOY` in the makefile to point to your server.

To build and deploy:

```bash
make
make update
```

As an example, this repository can be built as-is.

Warning: by design, anything deleted locally will be deleted on the server.

[jtsense]: http://jtsense.com
[pandoc]: http://pandoc.org/
[jemdoc]: http://jemdoc.jaboc.net/
[jemdoc-mj]: http://www.mit.edu/~wsshin/jemdoc+mathjax.html
[jem-press]: https://scottsievert.com/jem-press/
