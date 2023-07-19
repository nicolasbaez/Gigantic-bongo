# Gigantic-bongo
Invisible forces

![buh](https://github.com/nicolasbaez/Gigantic-bongo/blob/main/xp009.gif)
```javascript
w = 500;
h = w / 2;
k = 0;
setup = (_) => createCanvas(w, w, WEBGL);
draw = (_) => {
  background(0);
  noFill();
  for (i = h * 0.1; i < h * 0.9; i += h * 0.2) {
    rotateX(k);
    rotateY(k / 2);
    stroke(sin(k * i) * h, noise(k) * h, i);
    sphere(i, 3, 5);
  }
  k += 0.02;
};
function keyPressed() {
  if (key === "s") {
    saveGif("xp009.gif", 628, { delay: 0, units: "frames" });
  }
}
