# htm.JavaScript
This is a port of the [numenta/nupic](https://github.com/numenta/nupic) port [htm.java](https://github.com/numenta/htm.java) to JavaScript.

##Disclaimer
This project is work in progress and subject to frequent changes. Sometimes it might even be broken.

## Goal
Run NuPIC in a browser (For now Firefox only, due to extensive use of the ECMAScript 6 features such as Set and Map data structures)

## Usage
Clone or download ZIP

Alternative 1:

Load qt_interactive.html from the file system into Firefox (no web server needed). No web workers are used, so debugging with e.g. Firebug is supported. No browser freeze due to input presentation. This alternative is not available vor HelloSP.


Alternative 2:

1. Unpack into the web root folder of your favorite web server. With XAMPP the result should look like
   - htdocs/foo/bar/baz/nupic/...
   - ...
   - htdocs/foo/bar/baz/sp.html
   - htdocs/foo/bar/baz/qt.html

2. Start the web server

3. Load http://localhost/foo/bar/baz/sp.html or http://localhost/foo/bar/baz/qt.html with Firefox 

This alterbative uses web workers to avoid browser freeze, so debugging is difficult.


Alternative 3: 

Load sp_dbg.html or qt_dbg.html from the file system without using a web server. Allows the use of a debugger. This variant is closest to the Java original. Drawback: Browser freezes.

Currently htm.JavaScript reproduces both the "HelloSP" (sp.html or sp_dbg.html) and "QuickTest" (qt_interactive.html, qt.html, qt_dbg.html) demos from htm.java which illustrate SDRs, spatial pooling and temporal memory. 
