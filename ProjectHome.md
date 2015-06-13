# Overview #
Supported Multi URL requests for ApacheBench. You can set URL list as '-L filename' and
also confirm response of document length for each requests.

# Install #
Just replace "ab.c" on your apache source files, and build it again. Normally, just do as follows.

> cp ab.c /usr/local/src/httpd-2.x.xx/support<br>
<blockquote>cd /usr/local/src/httpd-2.x.xx/support<br>
make</blockquote>

<h1>Usage</h1>
This ApacheBench supports multi URLs(Max:20000URLs) like next.<br>
<br>
<blockquote>./ab -c 1 -n 10 -L urls.txt</blockquote>

In this case, ApacheBench picks up URLs from "urls.txt" and send requests. Also, confirm responses of document length for each requests. But the domain name of the URLs must be same as first URL at the URL list.<br>
<br>
<blockquote>e.g.)<br>
<a href='http://test.com/index.html'>http://test.com/index.html</a> <br>
<a href='http://test.com/top.html'>http://test.com/top.html</a> <br>
<a href='http://test.com/about.html'>http://test.com/about.html</a> <br></blockquote>

And if you don't use "-L" option, ApacheBench works as normal version.