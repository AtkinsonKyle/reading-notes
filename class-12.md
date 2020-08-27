# Daily Reading 12
### Chart.js
- Download Chart.js on [this page](https://github.com/nnnick/Chart.js)
- Need `<canvas>` node to render the chart(`<canvas>` reuires a closing tag)
- Look at [the contributing guidelines](https://github.com/chartjs/Chart.js/blob/master/docs/developers/contributing.md) first before pull requesting or submitting an issue
- Chart.js is available under the MIT License
- If we want to apply colors to a shape, there are two important properties we can use: `fillStyle` and `strokeStyle`
  - `fillstyle` style used when filling shapes
  - `strokeStyle` style for shapes' outlines
<br>

#### Example of Chart.js
<p> This takes a look at at two intersecting rectangles, one of which is alpha transparent.</p>

```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8"/>
  <script type="application/javascript">
    function draw() {
      var canvas = document.getElementById('canvas');
      if (canvas.getContext) {
        var ctx = canvas.getContext('2d');

        ctx.fillStyle = 'rgb(200, 0, 0)';
        ctx.fillRect(10, 10, 50, 50);

        ctx.fillStyle = 'rgba(0, 0, 200, 0.5)';
        ctx.fillRect(30, 30, 50, 50);
      }
    }
  </script>
 </head>
 <body onload="draw();">
   <canvas id="canvas" width="150" height="150"></canvas>
 </body>
</html>

```

#### Quadratic Bezier Curves
<p> Multiple quadratic bezier curves render a speech bubble in this example</p>

```
function draw() {
  var canvas = document.getElementById('canvas');
  if (canvas.getContext) {
    var ctx = canvas.getContext('2d');

    // Quadratric curves example
    ctx.beginPath();
    ctx.moveTo(75, 25);
    ctx.quadraticCurveTo(25, 25, 25, 62.5);
    ctx.quadraticCurveTo(25, 100, 50, 100);
    ctx.quadraticCurveTo(50, 120, 30, 125);
    ctx.quadraticCurveTo(60, 120, 65, 100);
    ctx.quadraticCurveTo(125, 100, 125, 62.5);
    ctx.quadraticCurveTo(125, 25, 75, 25);
    ctx.stroke();
  }
}

```

#### createPattern
<p>Image's onload handler is worth noting. Ensures the image is loaded before it is assigned to the pattern</p>

```
function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');

  // create new image object to use as pattern
  var img = new Image();
  img.src = 'https://mdn.mozillademos.org/files/222/Canvas_createpattern.png';
  img.onload = function() {

    // create pattern
    var ptrn = ctx.createPattern(img, 'repeat');
    ctx.fillStyle = ptrn;
    ctx.fillRect(0, 0, 150, 150);

  }
}

```