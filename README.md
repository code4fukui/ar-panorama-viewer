# ar-panorama-viewer

## usage

### demo

- https://code4fukui.github.io/ar-panorama-viewer/

### with src

- https://code4fukui.github.io/ar-panorama-viewer/?src=panorama-asakura-flip.jpg

### with option

- https://code4fukui.github.io/ar-panorama-viewer/?src=panorama-asakura-flip.jpg&tlen=340&h=3&r=3

## option

```js
<script type="module">
const param = new URL(location.href).searchParams;
const tlen = param.get("tlen") || 280;
const y = param.get("y") || 1.5;
const p = {
  src: param.get("src") || "panorama-asakura-flip.jpg",
  "theta-length": tlen,
  "theta-start": (360 - tlen) / 2,
  height: param.get("h") || 1.4,
  radius: param.get("r") || 1.5,
};
for (const name in p) {
  cylinder.setAttribute(name, p[name]);
}
cylinder.setAttribute("position", `0 ${y} 0`);
```
