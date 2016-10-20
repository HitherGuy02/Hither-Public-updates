# Hither-Public-updates
Updates for how my web browser hither is going (with binaries(app files) included).

###Features
 - ***CUSTOM*** tabs
 - Internet Access 
 - Bookmarks
 - History
 - Downloads

###For Web Developers
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
It would have a textfield that had the text "qwertyuiop", a button with the title "qwertp", and a web view with the page www.google.com loading.
