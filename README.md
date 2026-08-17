# GG-Bond — 刘昶 个人主页

## 预览

纯静态页面，无需构建工具。直接双击 `index.html` 即可，或用任意静态服务器：

```bash
python3 -m http.server 8000
# 然后打开 http://localhost:8000
```

## 个性化内容

所有内容集中在一处：`index.html` 顶部的 `window.SITE` 对象。

```js
window.SITE = {
  name: "刘昶", nameEn: "Chang Liu",
  title: "AI Product Manager",
  email: "lc15716951535@gmail.com",
  socials: [ /* { label, url } */ ],
  projects: [ /* { title, tag, description, stack } */ ],
  whatIDo: [ /* { title, desc } */ ],
  platforms: [ /* { name, short, desc, qr? 或 url } */ ],   // 公众号 / 人人都是产品经理
  articles: [ /* { title, platform, url, date } */ ]        // 文章列表
};
```

改完刷新即可。

## 页面结构

- 导航 / Hero（名字 + AI Product Manager）
- 关于我（About Me）
- 精选项目（Featured Projects）：爱支招、ExplainBack
- 我在做什么（What I Do）：Product / AI Product / Evaluation / Build & Ship
- 文章与思考（Writings）：公众号 + 人人都是产品经理 + 文章列表
- 联系（Contact）

## 待替换的占位内容

1. **公众号二维码**：`platforms` 里的 `qr: ""`，把二维码图片路径填进去即可（如 `qr: "qrcode.png"`）
2. **公众号链接**：`socials` 里的 `公众号 url: "#"`
3. **文章**：`articles` 里的标题、链接、日期都是示例

## 设计要点（源自 Discord 模板 · 浅色模式）

- **配色**：淡紫灰 `#f2f3f7` + blurple `#5865f2` + 近黑文字 `#1e1f22`
- **字体**：Nunito（粗圆标题，替代 Ginto Nord）+ Inter（正文，替代 gg sans）
- **动效**：极光 blob 漂移、标题渐入、名字渐变流光、顶部滚动进度条、卡片 hover、滚动出现
- **圆角**：12/16/20px 卡片 + 药丸按钮
