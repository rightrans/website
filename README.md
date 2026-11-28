# Rightrans Inc. — 公司网站 / Company website

rightrans.com 的网站源文件。**目前是草稿，尚未上线**（GitHub Pages 未开启）。

## 页面结构

| 文件 | 页面 |
|---|---|
| `index.html` / `zh.html` | 首页（英文 / 中文）：公司介绍、三项服务、我们的承诺、创始人、联系表单 |
| `agency.html` / `zh-agency.html` | 服务一：海外销售代理（帮工厂把产品卖进国际市场） |
| `sourcing.html` / `zh-sourcing.html` | 服务二：全球采购（帮采购商找到可靠货源） |
| `parts.html` / `zh-parts.html` | 服务三：老旧件替代（停产、难买零件的替代品） |
| `privacy.html` / `zh-privacy.html` | 隐私政策与法律声明 |
| `404.html`、`robots.txt`、`sitemap.xml` | 找不到页面、搜索引擎设置 |
| `fonts/`、`images/` | 自托管字体（不依赖 Google Fonts，国内也能正常加载）、照片、网站图标、分享图 |
| `design/` | 设计稿源文件（Claude 设计画布格式，`.dc.html`），`_config.yml` 已设置为不发布 |

纯静态 HTML，无需构建。样式写在页面内，菜单、下拉和表单用页面底部的一小段 JavaScript。

## 联系表单

`index.html` 和 `zh.html` 底部脚本里有一行 `var FORM_ENDPOINT='';`。
- 留空时：点“发送”会打开访客的邮件应用，自动填好内容，发到 info@rightrans.com。
- 注册 Formspree 后，把表单地址（形如 `https://formspree.io/f/xxxx`）填进去，中英文两页都要填。之后表单直接在页面上提交，并显示“已收到”。

## 上线前待办

1. 填写或删除剩余占位内容：搜索 `[填写`、`[Fill in`。
2. 接 Formspree（见上）。
3. 开启 GitHub Pages，在仓库根目录加 `CNAME` 文件（内容 `rightrans.com`），并把 rightrans.com 指向 GitHub Pages。修改 DNS 时只改网站相关的记录（A / CNAME），**不要动 MX、SPF、DKIM、DMARC 等邮件记录**，否则公司邮箱会失效。
4. 上线后在 Google Search Console 提交 `sitemap.xml`。
