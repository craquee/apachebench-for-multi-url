## Apachebench-for-multi-URL
Automatically exported from code.google.com/p/apachebench-for-multi-url

## Overview
Supported Multi URL requests for ApacheBench. You can set URL list as '-L filename' and 
also confirm response of document length for each requests. 

## Install 
Just replace "ab.c" on your apache source files, and build it again. Normally, just do as follows.

cp ab.c /usr/local/src/httpd-2.x.xx/support <br>
cd /usr/local/src/httpd-2.x.xx/support <br>
make <br>

## Usage
This ApacheBench supports multi URLs(Max:20000URLs) like next. 

`./ab -c 1 -n 10 -L urls.txt      ` 

In this case, ApacheBench picks up URLs from "urls.txt" and send requests. Also, confirm responses of document length for each requests. But the domain name of the URLs must be same as first URL at the URL list. 

e.g.)<br>
http://test.com/index.html <br> 
http://test.com/top.html <br>
http://test.com/about.html <br> 

And if you don't use "-L" option, ApacheBench works as normal version. 
