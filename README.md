Liffy
=====

Liffy is a Local File Inclusion Exploitation tool.  

Current features include: 

  - data:// for code execution
  - expect:// for code execution
  - input:// for code execution
  - filter:// for arbitrary file reads
  - /proc/self/environ for code execution in CGI mode
  - Apache access.log poisoning
  - Linux auth.log SSH poisoning
  - Direct payload delivery with no stager
  - Support for absolute and relative paths 



Install
=======

Liffy requires the following libraries: requests, argparse, blessings, urlparse

In order to host the payload you may use Node's HTTP server: https://github.com/nodeapps/http-server

Or you can simply spawn python's SimpleHTTPServer in /tmp on port 8000.  Further development of the tool will eventually include spawning a built-in web server in order to download, for now you can adjust the location and port in the source code for your needs.  These can be changed in core.py under the execute functions.


Example Usage 
==============

./liffy --url http://target/pdfs/vulnerable.php?= --data
