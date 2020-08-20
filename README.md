<p align="center">
  <img src="/assets/animetv.png" width="70" />
</p>
<p align="center">⭐⭐⭐⭐⭐</p>
<h1 align="center">Anime TV API</h1>
<h4 align="center"><a href="https://github.com/LaksCastro/anime-tv-api/tree/master/app"><code>Analyse Extracted Code</code></a></h4>
<p align="center">Anime TV é um  aplicativo utilizado para Stream de animes totalmente grátis mas com anúncios. E este repositório é a documentação não oficial da API utilizada para buscar os dados dos animes.</a></p>
<p align="center">
  <img  src="https://img.shields.io/badge/type-api_endpoints-purple" alt="Application Category" />
  <img  src="https://img.shields.io/badge/status-working_fine-success" alt="Repo Status" />
  <img  src="https://img.shields.io/badge/where_from-doctpit_web_platform-blue" alt="Repo Ref" />
</p>

### Starting
- Smart tip on render the Pixel Arts: all image url's will have a small size by default (64x64), so, you may have problems to render it on a normal `<img>` HTML tag. To fix this, continue using the `<img>` tag, but with a additional CSS property:
```css
/* BAD - ALL IMAGES WILL BE SHOW AS LOW QUALITY */
img {
  width: 930px;
  height: 930px;
}

/* GOOD - ALL IMAGES WILL BE REPRESENTED WITH A GOOD QUALITY USING A PIXEL IMAGE ALGORITHM */
img {
  width: 930px;
  height: 930px;
  image-rendering: pixelated;
}

```
