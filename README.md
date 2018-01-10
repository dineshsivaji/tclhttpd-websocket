# tclhttpd-websocket


I have asked a question about implementing websockets with web-browser being a websocket client and 
Tcl being a websocket server in stackoverflow (https://stackoverflow.com/questions/48128997/tcl-server-with-websocket-client-on-browser)


Then Mr.Donal Fellows directed me to the following Wiki page.

http://wiki.tcl.tk/40442

Thanks to Mr.Jeff Smith who actually posted the starkit version of it. I have just unwrapped the code.

I have made it compatible with Tcl8.4 (as it was my requirement) by altering the **binary scan/format** commands.

The Tcl8.5 version has support for unsigned numbers by adding character **u** in the formatString. 
For ```binary scan```, I have used `bscan` procedure which is taken from http://wiki.tcl.tk/4180. 
For ```binary format```, I have changed the format specifier, ```u``` to ```*```. 

