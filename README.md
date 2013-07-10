p5-nginx-minify
===============

Nginx Perl Minify [CSS / JS / HTML5]

Depending on FreeBSD
===============
FreeBSD
```bash
$ portmaster textproc/p5-CSS-Minifier-XS textproc/p5-JavaScript-Minifier-XS textproc/p5-HTML-Packer
```
Ubuntu/Debian
```bash
apt-get install libcss-minifier-xs-perl libjavascript-minifier-xs-perl libhtml-packer-perl
```

Install
===============
nginx.conf -> /etc/nginx/nginx.conf
mkdir /etc/nginx/perl
Minify.pm -> /etc/nginx/perl/

TODO
===============
* […] $content_type = "text/html" on fastcgi/proxy after compress
* […] algorithm cache select path for static

Known Problems
===============
http://wiki.nginx.org/HttpPerlModule#Known_Problems
* If a Perl module performs protracted operation, (for example DNS lookups, database queries, etc), then the worker process that is running the Perl script is completely tied up for the duration of script. Therefore embedded Perl scripts should be extremely careful to limit themselves to short, predictable operations.
* It's possible for Nginx to leak memory if you reload the configuration file (via 'kill -HUP <pid>').
