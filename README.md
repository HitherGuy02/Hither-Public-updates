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
        var f = t.openWindowWithContents_("Textfield..0,,0,,200,,20!!qwertyuiop~~yes//Button..0,,40,,50,,20!!qwertyuiop//Webview..0,,70,,400,,400!!www.google.com//View..0,,0,,500,,300!!Button$$0@@5@@100@@40--button**View$$24@@3@@400@@700--//Button..30,,30,,30,,30!!");
        
    };
</script>
```
It would have:
 - a textfield (`Textfield..`) with the measurements (x = 0, y = 0, width = 200, height = 20) (`0,,0,,200,,20`) with the text "qwertyuiop" (`!!qwertyuiop`) in it. It will be editable (`~~yes`)
 - tell it to end (`//`)
 - a button (`Button..`) with the measurements (x = 0, y = 40, width = 50, height = 20) (`0,,40,,50,,20`) with the title "qwertyuiop" (`!!qwertyuiop`)
 - tell it to end (`//`)
 - a webview (`Webview..`) with the measurements (x = 0, y = 70, width = 400, height = 400) (`0,,70,,400,,400`) loading the page www.google.com (`!!www.google.com`)
 - tell it to end (`//`)
 - a view (`View..`) with the measurements (x = 0, y = 0, width = 500, height = 300) (`0,,0,,500,,300`) that includes :
     - a button (`Button$$`) with the measurements (x = 0, y = 40, width = 50, height = 20) (`0@@5@@100@@40`) with the title "button" (`--button`)
     - tell it to end (`**`)
     - a view (`View$$`) with the measurements (x = 24, y = 3, width = 400, height = 700) (`24@@3@@400@@700`) that doesn't include any other views or anything of the like (`--`)
 - tell it to end (`//`)
 - a button (`Button..`) with the measurements (x = 30, y = 30, width = 30, height = 30) (`30,,30,,30,,30`) with no title (`!!`)

***The measurements are in pixels.***

##Supported Types ***(Case Sensitive)***
 - Webview
 - Button
 - Textfield
 - View
