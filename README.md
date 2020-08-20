
#### Starting
- Smart tip on render the Pixel Arts: all image url's will have a small size by default (64x64), so, you may have problems to render it on a normal `<img>` HTML tag. To fix this, continue using the `<img>` tag, but with a additional CSS property:
```css
/* BAD - ALL IMAGES WILL BE SHOW AS LOW QUALITY */
img {
  width: 930px;
  height: 930px;
}

/* GOOD - ALL IMAGES WILL BE REPRESENTED WITH QUALITY GOOD USING A PIXELATED ALGORITHM */
img {
  width: 930px;
  height: 930px;
  image-rendering: pixelated;
}

```
