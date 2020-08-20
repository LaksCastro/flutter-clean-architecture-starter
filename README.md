<p align="center">
  <img src="/assets/dot-logo.png" width="150" />
</p>
<p align="center">⭐⭐⭐⭐⭐</p>
<h1 align="center">Dotpict</h1>
<h4 align="center"><a href="https://dotpict.net/"><code>Analyse Dotpict Platform</code></a></h4>
<p align="center">Dotpict is a complete web and mainly mobile platform to share, like, post, create and draw Pixel Arts. And its is a unnoficial documentation about the API used by Dotpict.</p>
<p align="center">
  <img  src="https://img.shields.io/badge/type-api_endpoints-purple" alt="Application Category" />
  <img  src="https://img.shields.io/badge/status-working_fine-success" alt="Repo Status" />
  <img  src="https://img.shields.io/badge/where_from-doctpit_web_platform-blue" alt="Repo Ref" />
</p>

### Considerations

### Documentation

- [Setup](#setup)
- Get trending arts
- Get recent arts
- Get arts from a user


#### - Setup

- Smart tip on render the Pixel Arts: all image url's will have a small size by default (64x64), so, you may have problems to render it on a normal `<img>` HTML tag. To fix this, continue using the `<img>` tag, but with a additional CSS property:
```css
/* BAD - ALL IMAGES WILL BE SHOW AS LOW QUALITY */
img {
  width: 930px;
  height: 930px;
}

/* GOOD - ALL IMAGES WILL BE RENDERED WITH A GOOD QUALITY USING A PIXEL IMAGE ALGORITHM */
img {
  width: 930px;
  height: 930px;
  image-rendering: pixelated;
}

```
