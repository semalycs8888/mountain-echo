# 山回 · 雾里弦声

Static gallery (vinyl + blues). Hosted on GitHub Pages.

## Live site

https://semalycs8888.github.io/mountain-echo/

## COS cloud save

In the page editor, fill Tencent COS settings and click 保存到云端.

Bucket CORS must allow the Pages origin. See `cos-cors.json` — in COS console: Bucket → 安全管理 → 跨域访问 CORS, add origin `https://semalycs8888.github.io` with GET/PUT/POST/HEAD, headers `*`, expose ETag and Content-Length.

## Deploy

Push to `main`; GitHub Pages serves from the repository root.
