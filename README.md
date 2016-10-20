# Hither-Public-updates
Updates for how my web browser hither is going (with binaries(app files) included).

#Features
 - ***CUSTOM*** tabs
 - Internet Access 
 - Bookmarks
 - History
 - Downloads

#For Web Developers
Hither is very special in that it allows the use of javascript to open windows.
If you had 
```html
<script type="text/javascript">
    function openVindow() {
        var t = window.webEl;
        var f = t.openWindowWithContents_("Textfield..0,,0,,200,,20!!qwertyuiop//Button..0,,40,,50,,20!!qwertp//Webview..0,,70,,400,,400!!www.google.com");
        
    };
</script>
```
It would have a textfield that had the text "qwertyuiop" that appeared at *(x = 0, y = 0, width = 200, height = 20)*, a button with the title "qwertp" that appeared at *(x = 0, y = 40, width = 50, height = 20)*, and a web view with the page www.google.com loading that appeared at *(x = 0, y = 70, width = 400, height = 400)*. ***The measurements are in pixels.***

##Supported Types ***(Case Sensitive)***
 - Webview
 - Button
 - Webview
 - View
 - 
