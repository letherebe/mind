```javascript
// Draws animated, colorful rings expanding from the center of the canvas
const canvas = document.createElement('canvas');
document.body.appendChild(canvas);
canvas.width = canvas.height = 400;
const ctx = canvas.getContext('2d');
let t = 0;
function draw() {
  ctx.clearRect(0,0,400,400);
  for(let i=0;i<8;i++){
    ctx.beginPath();
    let r = 20 + 30*i + 18*Math.sin(t/20 + i);
    ctx.arc(200,200,r,0,2*Math.PI);
    ctx.strokeStyle = `hsl(${(i*45 + t)%360},70%,60%)`;
    ctx.lineWidth = 10 - i;
    ctx.globalAlpha = 0.6 - i*0.06;
    ctx.stroke();
  }
  ctx.globalAlpha = 1;
  t++;
  requestAnimationFrame(draw);
}
draw();
```