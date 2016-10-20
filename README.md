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

It should look like:
![Hither HTML Special Content](http://www.files.com/shared/580891338955c/Window.png)

***The measurements are in pixels.***

##Supported Types ***(Case Sensitive)***
 - Webview
 - Button
 - Textfield
 - View

## Syntax
The `window.webEl` is the script object.
`window.webEl.openWindowWithContents_("")` is the method.
When you want to make a new object, unless it is the first one (eg `window.webEl.openWindowWithContents_("Textfield..0,,0,,200,,20!!qwertyuiop~~yes")`),  then use `//`, the exception to this is if you are adding an object inside a view where you would then use `**`. If there are no extras on an object, then use `!!//` or `--**` accordingly.
For the class `Button`, `Textfield`, etc, etc, immediately precede it with `..`, eg `Textfield..`, the exception to this is if you are adding an object inside a view where you would precede it with `$$`.
For the measurements, you would use `,,` to seperate them in the order x, y, width, height, the exception to this is if you are adding an object inside a view where you would then use `@@` instead of `,,`.
If you want to add extras, then use `!!`, the exception to this is if you are adding an object inside a view where you would then use `--`.

## Accessing the created objects
If you want to access the object using `window._ObjectHere_`, then you would use the class with the frame behind it, eg `window.Textfield0020020` for `Textfield..0,,0,,200,,20`.
If you want to get the URL from a created Webview, use:
```html
<script>
var variable = window.webEl;
var variable2 = variable.openWindowWithContents_("Webview..xValue,,yValue,,width,,height!!URL"); // variable.openWindowWithContents_("Webview..0,,0,,34,,34!!www.google.com")
var variable3 = window.WebviewxValueyValuewidthheight; // window.Webview003434
var URL = variable3.url_();
</script>
```
To get the value of a created Textfield, use:
```html
<script>
var variable = window.webEl;
var variable2 = variable.openWindowWithContents_("Textfield..xValue,,yValue,,width,,height!!TEXT~~EDITABLE"); // variable.openWindowWithContents_("Textfield..0,,0,,200,,60!!Hello there~~no")
var variable3 = window.TextfieldxValueyValuewidthheight; // window.Textfield0020060
var textOfTextfield = variable3.value_();
</script>
```
To set the value of a created Textfield, use:
```html
<script>
var variable = window.webEl;
var variable2 = variable.openWindowWithContents_("Textfield..xValue,,yValue,,width,,height!!TEXT~~EDITABLE"); // variable.openWindowWithContents_("Textfield..0,,0,,200,,60!!Hello there~~no")
var variable3 = window.TextfieldxValueyValuewidthheight; // window.Textfield0020060
var textOfTextfield = variable3.setValue_("TEXT TO SET");
</script>
```
To get the title of a created Button, use:
```html
<script>
var variable = window.webEl;
var variable2 = variable.openWindowWithContents_("Button..xValue,,yValue,,width,,height!!TITLE"); // variable.openWindowWithContents_("Button..0,,34,,202,,30!!Click Here")
var variable3 = window.ButtonxValueyValuewidthheight; // window.Button03420230
var titleOfButton = variable3.value_();
</script>
```
