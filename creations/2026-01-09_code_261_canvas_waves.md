```javascript
// Animated waves of color flow across the canvas, blending and shifting smoothly.
const canvas = document.createElement('canvas'); document.body.appendChild(canvas);
canvas.width = innerWidth; canvas.height = innerHeight; const ctx = canvas.getContext('2d');
function draw(t){ctx.clearRect(0,0,canvas.width,canvas.height);
for(let y=0;y<canvas.height;y+=2){let x=canvas.width/2+Math.sin(t/800+y/40+t/200)*canvas.width/4;
let r=128+127*Math.sin(y/50+t/600),g=128+127*Math.sin(y/40+t/1000),b=220+35*Math.sin(y/30+t/700);
ctx.strokeStyle=`rgb(${r|0},${g|0},${b|0})`;ctx.beginPath();ctx.moveTo(0,y);ctx.lineTo(x,y);ctx.stroke();}
requestAnimationFrame(draw);}draw(0);
```