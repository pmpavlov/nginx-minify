p5-nginx-minify
===============

Nginx Perl Minify [CSS / JS / HTML5]

Depending on FreeBSD
===============
* `/usr/ports/textproc/p5-CSS-Minifier-XS`
* `/usr/ports/textproc/p5-JavaScript-Minifier-XS`
* `/usr/ports/textproc/p5-HTML-Packer`

Install
===============
```bash
$ portmaster textproc/p5-CSS-Minifier-XS textproc/p5-JavaScript-Minifier-XS textproc/p5-HTML-Packer
```

TODO
===============
* […] $content_type = "text/html" on fastcgi/proxy after compress
* […] algorithm cache select path for static

Known Problems
===============
http://wiki.nginx.org/HttpPerlModule#Known_Problems
* If a Perl module performs protracted operation, (for example DNS lookups, database queries, etc), then the worker process that is running the Perl script is completely tied up for the duration of script. Therefore embedded Perl scripts should be extremely careful to limit themselves to short, predictable operations.
* It's possible for Nginx to leak memory if you reload the configuration file (via 'kill -HUP <pid>').
