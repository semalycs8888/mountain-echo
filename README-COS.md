# 腾讯云 COS 部署（山回 · 雾里弦声）

1. 创建存储桶（名称形如 `mountain-echo-1250000000`），开启「静态网站」，默认首页设为 `index.html`。
2. 配置 CORS：来源 `*`，方法含 PUT/GET/HEAD/POST，ExposeHeaders 含 `ETag`、`Content-Length`。
3. 上传本目录：`index.html`、`gallery.json`、`assets/`（可放在前缀如 `mountain-echo/`）。
4. 读写权限：站点文件与 `gallery.json`、`uploads/` 需能公共读（或走 CDN）。
5. 打开站点后点左上角「编辑内容」→ 填写 Region / Bucket / SecretId / SecretKey →「保存到云端」。
6. 自定义图片会上传到 `{前缀}uploads/`，文案写入 `{前缀}gallery.json`。

注意：浏览器里填永久密钥仅适合个人站；正式环境请改用 STS 临时密钥。
