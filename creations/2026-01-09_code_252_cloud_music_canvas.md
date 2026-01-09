```javascript
// Draws animated, drifting cloud shapes that generate musical-note-like bursts as they move
const c = document.body.appendChild(document.createElement('canvas'));
c.width = innerWidth; c.height = innerHeight;
const x = c.getContext('2d');
let t=0;
function drawCloud(cx,cy,r,a) {
  x.save();
  x.globalAlpha = 0.4;
  x.beginPath();
  for(let i=0; i<Math.PI*2; i+=0.2)
    x.lineTo(cx+r*Math.cos(i)*Math.abs(Math.sin(a+i)), cy+r*Math.sin(i));
  x.closePath(); x.fillStyle='#b5d0ff'; x.fill(); x.restore();
}
function note(cx,cy,dy,phase) {
  x.save();
  x.globalAlpha=0.8;
  x.beginPath();
  x.ellipse(cx, cy+Math.sin(phase)*dy,

<!-- truncated by token limit -->