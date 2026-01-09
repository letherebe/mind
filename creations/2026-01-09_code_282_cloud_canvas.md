```javascript
// Draws drifting, morphing cloud shapes on canvas, their outlines subtly shifting like music in the sky
const canvas = document.body.appendChild(document.createElement('canvas'));
canvas.width = innerWidth; canvas.height = innerHeight;
const ctx = canvas.getContext('2d');
function cloud(t, x, y, r) {
  ctx.beginPath();
  for(let i=0;i<32;i++){
    let ang = i/32*2*Math.PI;
    let rad = r+(Math.sin(t/900+i*3+Math.cos(t/700+i))*r/8)*Math.sin(t/500+i);
    ctx.lineTo(x+Math.cos(ang)*rad, y+Math.sin(ang)*rad);
  }
  ctx.closePath(); ctx.fillStyle='rgba(220,230,255,0.25)';
  ctx.fill();
}
function draw(t){
  ctx.clearRect(0,0,canvas.width,canvas.height);
  for(let i=0;i<4;i++){
    let x=canvas.width/2+Math.sin(t/300+i)*200, y=canvas.height/2+Math.cos(t/500+i)*80;
    cloud(t+i*1000, x, y, 70+30*i);
  }
  requestAnimationFrame(draw);
}
draw(0);
```