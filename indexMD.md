## Welcome to GitHub Pages

You can FFEF use the [editor on GitHub](https://github.com/omkarsnl/files/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown FERFis a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List



**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/omkarsnl/files/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

 ```css
button{height: 29px;width: 80px;padding-top: 12px;padding-bottom: 22px;}
html,body{font-family:Verdana,sans-serif;font-size:15px;line-height:1.5}html{overflow-x:hidden}
h6{font-size:16px;font-family:"Segoe UI",Arial,sans-serif;font-weight:500;margin:10px 0}
p {color: white;text-align: center;}
.om-serif{font-family:serif}
.om-wide{letter-spacing:4px}
.in1 {width: 90%;padding:8px 0px 2px 8px;font-size: 18px;}
.in2 {width: 90%;padding:8px 0px 2px 8px;font-size: 18px;}
.in1:focus,.in2:focus{border: black solid 2px;}
.w20 {float: left;width: 100%;background-color: darkgrey;}
.inline {float: left;padding: 5px 14px 5px;color: #000;}
/**********************slider css****************************/
#slidecontainer {width: 95%;}
.slider {-webkit-appearance: none;width: 95%;height: 15px;border-radius: 10px;background: red;outline: none;opacity: 0.7;-webkit-transition: .2s;transition: opacity .2s;margin-top: 8px;}
.slider:hover {opacity: 1;}
.slider::-webkit-slider-thumb {-webkit-appearance: none;appearance: none;width: 25px;height: 25px;border-radius: 50%;background: #fff;cursor: pointer;border: 1px solid #ccc;}
.slider::-moz-range-thumb {width: 25px;height: 25px;border-radius: 50%;background: #4CAF50;cursor: pointer;}
.omm2 {background-color: #8e8e8e;float: left;width: 100%;}
.om-container {padding: 0.01em 16px;}

@media (min-width: 1024px){
 .omm2 {width: 50%;}
}
@media (min-width: 1024px){
 .w20 {width: 20%;}
}

```
```
<div>
<h6>Import Values(Comma Seperated Values) From Sever File(.txt/.csv)</h6>
<button id="btn1" disabled>Import</button>
 <input id="in2" class="in2" type="url" oninput="intype()"  type="number"  placeholder="Enter URL https:/http:">

  <div class="w20 om-container " style="padding-bottom: 31px;">
   <h6>Face Level Input</h6>

    <input id="in1" class="in1" type="text" type="number" value="800000.00" name="number">
  </div>

  <div class="w20 om-container" style="padding-bottom: 38px;">
   <div id="slidecontainer">
   <h6>Face Scale: <span id="val"></span>%</h6>
   <input type="range" min="0" max="100" value="0" step="25" class="slider" id="Range">
   </div>
  </div>

  <div class="om-container omm2 " >
  <div>
    <h6 class="inline">Total Faces Output <p id="out1">Output1</p></h6>
    <h6 class="inline">Youth Factor Output <p id="out2">Output2</p></h6>
    <h6 class="inline">Age Factor Output <p id="out3">Output3</p></h6>
  </div>
  </div>
</div>
 ```
 ```javascript
var s = document.getElementById("Range");
var c = document.getElementById("val");
var a1 = document.getElementById("in1");
var b1 = document.getElementById("out1");
var b2 = document.getElementById("out2");
var b3 = document.getElementById("out3");
var b = c.innerHTML = s.value;
var top = 1.09989;
var bottom = 1.061105;
var tbrange = 0.038785;

s.oninput = function() {
 var b = c.innerHTML = s.value;
 $('.in1').number( true, 2 );
        var u4 = $('#in1').val();
  b=parseInt(b)     
switch (b) {
    case 25:
       b = c.innerHTML = s.value -5;
        break;
    case 75:
        b = c.innerHTML = s.value -5;
        break;
    default: 
        b = c.innerHTML = s.value;    
}
var u1=b1.innerHTML=(tbrange*u4).toFixed(2);
var u2=b2.innerHTML=((b/100)*u1).toFixed(2);
var u3=b3.innerHTML=(u1-u2).toFixed(2);
$('#out1,#out2,#out3').number( true, 2 );
}
a1.oninput = function() {
var u4 = $('#in1').val(); 
var u1=b1.innerHTML=(tbrange*u4).toFixed(2);
var u2=b2.innerHTML=((b/100)*u1).toFixed(2);
var u3=b3.innerHTML=(u1-u2).toFixed(2);
$('#out1,#out2,#out3').number( true, 2 );
}
 $('.in1').number( true, 2 );
var u4 = $('#in1').val();
var u1=b1.innerHTML=(tbrange*u4).toFixed(2);
var u2=b2.innerHTML=((b/100)*u1).toFixed(2);
var u3=b3.innerHTML=(u1-u2).toFixed(2);
$('#out1,#out2,#out3').number( true, 2 );
var url= "http://localhost/khk/Calculator/javascript/value.txt"
$(document).ready(function(){
$("button").click(function(){
var a2 = document.getElementById("in2");
var url=a2.value;
var m=$.get(url, function(data, status){
  var k=m.responseText;
  var arr = k.split(",");
   var t=arr[0];
   var u=arr[1];
   in1.value=t;
  b=u;
  c.innerHTML=s.value=b;
  var u4 = $('#in1').val();
var u1=b1.innerHTML=(tbrange*u4).toFixed(2);
var u2=b2.innerHTML=((b/100)*u1).toFixed(2);
var u3=b3.innerHTML=(u1-u2).toFixed(2);
$('#out1,#out2,#out3').number( true, 2 );
        });
    });
});

function intype() {
    document.getElementById("btn1").disabled = false;
}

```
