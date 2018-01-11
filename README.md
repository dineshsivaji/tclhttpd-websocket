# tclhttpd-websocket

# How to Run ?
Navigate to `bin` directory and execute the following command

`tclsh httpd.tcl -port 8016`

Here, `-port` is an optional field. The port number is defaulted to `8015`


Then open the following link in web browser which supports `WebSockets` (like latest version of Chrome or Firefox)

http://localhost:8016/websocket2.html 

Now, you can connect with the server and send some text message to it and the server will simply echo it back to the client. 

# History

I have asked a question about implementing websockets with web-browser being a websocket client and 
Tcl being a websocket server in stackoverflow (https://stackoverflow.com/questions/48128997/tcl-server-with-websocket-client-on-browser)


Then Mr.Donal Fellows directed me to the following Wiki page.

http://wiki.tcl.tk/40442

Thanks to Mr.Jeff Smith who actually posted the starkit version of it. I have just unwrapped the code.

I have made it compatible with Tcl8.4 (as it was my requirement) by altering the **binary scan/format** commands.

The Tcl8.5 version has support for unsigned numbers by adding character **u** in the formatString. 
For ```binary scan```, I have used `bscan` procedure which is taken from http://wiki.tcl.tk/4180. 
For ```binary format```, I have changed the format specifier, ```u``` to ```*```. 

