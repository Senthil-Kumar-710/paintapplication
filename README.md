# Web Page for Paint Application

## AIM:

To design a static website for Paint Application using HTML5 canvas.

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML,CSS and canvas.

### Step 3:

Write javascript to capture move events.

### Step 4:

Perform the drawing operation based on the user input.

### Step 5:

Validate the layout in various browsers.

### Step 6:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :

```
<!DOCTYPE html>
<html>
<body id="Content">
    <div id="Template">
<canvas id="myCanvas" width="500" height="500" onclick="showCoords(event)"></canvas></div>
<center>
<button onclick="shape=1" id="Shapes">Circle</button>
<button onclick="shape=2" id="Shapes">Outline Circle</button>
<button onclick="shape=3" id="Shapes">Square</button>
<button onclick="shape=4" id="Shapes">Outline Square</button>
<button onclick="shape=5" id="Shapes">Triangle</button>
<button onclick="shape=6" id="Shapes">Outline Triangle</button>
<br>
<button onclick="size()" id="Shapes">Change size</button>
</center>
<center>
<button onclick="change_color(this)" id="Colour" style="background: rgb(255, 255, 255);"></button>
<button onclick="change_color(this)" id="Colour" style="background: rgb(255, 72, 72);"></button>
<button onclick="change_color(this)" id="Colour" style="background: rgb(255, 115, 1);"></button>
<button onclick="change_color(this)" id="Colour" style="background: rgb(252, 255, 60);"></button>
<button onclick="change_color(this)" id="Colour" style="background: rgb(94, 255, 45);"></button>
<button onclick="change_color(this)" id="Colour" style="background: rgb(7, 184, 1);"></button>
<button onclick="change_color(this)" id="Colour" style="background: rgb(49, 231, 255);"></button>
<button onclick="change_color(this)" id="Colour" style="background: rgb(46, 112, 255);"></button>
<button onclick="change_color(this)" id="Colour" style="background: rgb(213, 76, 255);"></button>
<button onclick="change_color(this)" id="Colour" style="background: rgb(153, 0, 255);"></button>
<button onclick="change_color(this)" id="Colour" style="background: rgb(54, 0, 124);"></button>
<button onclick="change_color(this)" id="Colour" style="background: rgb(0, 0, 0);"></button>
</center>
    <div class="fbox">
    <div class="footer">
<center>
<p>Made By-
<a>Senthil Kumar S</a></p></center></div></div>
<script>
const canvas = document.getElementById("myCanvas");
const ctx = canvas.getContext("2d");
ctx.fillStyle = "#FF0000";
canvas.height = canvas.width;
ctx.transform(1, 0, 0, -1, 0, canvas.height);
let xMax = canvas.height;
let yMax = canvas.width;
let csize= 20;
let sqsize= 50;
let tsize=30;
let shade="black";
function size()
{   
if (shape==1 ||shape==2){
    let c=prompt("Enter size of the circle", "ex:86");
    csize=c;
} 
if (shape==3 ||shape==4){
    let s=prompt("Enter size of the square", "ex:95");
    sqsize=s;
}
if (shape==5 || shape==6){
    let t=prompt("Enter size of the triangle","ex:20");
    tsize=t;
}
}
function change_color(element){
    shade=element.style.background;
}

    function showCoords(event)

    {
    var x=event.clientX-545;
    var y=yMax-event.clientY;
    var coords="X coords: " + x + ", Y coords: " + y;
    document.getElementById("demo").innerHTML=coords;
    
        if (shape==1){
            ctx.beginPath();
            ctx.arc(x, y, csize, 0, 2 * Math.PI);
            ctx.fillStyle=shade;
            ctx.fill();
        }
        if (shape==2){
            ctx.beginPath();
            ctx.arc(x, y, csize, 0, 2 * Math.PI);
            ctx.strokeStyle=shade;
            ctx.stroke();
        }
        if (shape==3){
            ctx.beginPath();
            ctx.rect(x-(sqsize/2),y-(sqsize/2), sqsize,sqsize);
            ctx.fillStyle=shade;
            ctx.fill();
        }
        if (shape==4){
            ctx.beginPath();
            ctx.rect(x-(sqsize/2),y-(sqsize/2), sqsize,sqsize);
            ctx.strokeStyle=shade;
            ctx.stroke();
        }
        if (shape==6){
            ctx.beginPath();
            ctx.moveTo(x, y);
            ctx.lineTo(x-(tsize/2),y-(tsize*0.86602));
            ctx.lineTo(x+(tsize/2),y-(tsize*0.86602));
            ctx.lineTo(x,y)
            ctx.strokeStyle=shade
            ctx.stroke();
        }
        if (shape==5){
            ctx.beginPath();
            ctx.moveTo(x, y);
            ctx.lineTo(x-(tsize/2),y-(tsize*0.86602));
            ctx.lineTo(x+(tsize/2),y-(tsize*0.86602));
            ctx.fillStyle=shade
            ctx.fill();
        }
    
    
    }

</script>
<center><p id="demo" style="color: white;"></p></center>
<style>
#Content{
    background-color: #00e1ff;
}
#Template{
    padding-left: 545px;
   
}
#myCanvas{
    background-color: #ffffff86; 
    box-shadow: inset 0 0 5px #b6b6b6;
    backdrop-filter: blur(15px);
    border-radius: 10px;
    border: 1px solid #ffffff;
}
#Shapes{
    background-color: #11ff00;
    border: 2px solid rgb(255, 255, 255);
    border-radius: 25px;
    color: white;
    padding: 15px 32px;
    text-align: center;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
}
#Colour{
    border: 2px solid #ffffff;
    border-radius: 25px;
    padding: 25px 25px;
    text-align: center;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
}
<br>
.footer p {
    margin: 0;
    line-height: 26px;
    font-size: 15px;
    color: #990099;
}
</style>
</body>
</html>
```

## OUTPUT:

![canvas](https://user-images.githubusercontent.com/93860256/150333703-42cdbb51-66a9-4867-b8c1-7c0c65f22117.PNG)


## Result:

Thus a website is designed and validated for paint application using HTML5 canvas.
