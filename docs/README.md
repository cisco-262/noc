# OpsHome 产品主页部署说明

## 文件用途

- `index.html`：产品主页，包含四个产品的标准 HTML 直链、canonical、Open Graph 和 JSON-LD 结构化数据。
- `styles.css`：蓝色科技风响应式样式，无第三方依赖。
- `script.js`：移动菜单、滚动状态和渐入动画。
- `og-opshome-products.png`：LinkedIn、X 等平台使用的 1200×630 分享图。
- `favicon.svg`：网站图标。
- `robots.txt`：允许搜索引擎抓取，并声明 Sitemap。
- `sitemap.xml`：根域首页 Sitemap。
- `site.webmanifest`：网站基础清单。
- `404.html`：自定义 404 页面。

## 部署

将压缩包内的全部文件上传到 `opshome.run` 网站根目录，确保访问关系如下：

- `https://opshome.run/` → `index.html`
- `https://opshome.run/styles.css`
- `https://opshome.run/script.js`
- `https://opshome.run/robots.txt`
- `https://opshome.run/sitemap.xml`
- `https://opshome.run/og-opshome-products.png`

不要再将根域 301/302 跳转到 `app.opshome.run`，否则这个产品总入口不会被索引。

## 部署后的检查

1. 用浏览器打开 `https://opshome.run/`，确认返回 HTTP 200。
2. 查看网页源代码，确认四个产品链接直接存在于 HTML 中。
3. 打开 `https://opshome.run/robots.txt` 和 `https://opshome.run/sitemap.xml`。
4. 在 Google Search Console 提交：`https://opshome.run/sitemap.xml`。
5. 使用 URL 检查测试 `https://opshome.run/`，测试实际网址后仅请求一次编入索引。
6. 在现有四个产品网站页脚保留返回 `https://opshome.run/` 的链接，形成双向站内链接。

## 可选修改

网页中的产品说明和链接集中在 `index.html` 中。当前产品入口为：

- OpsHome NOC：`https://app.opshome.run/`
- Domain Health Inspector：`https://domain.opshome.run/`
- SSL Reminder：`https://ssl.opshome.run/`
- WiFi Health Check：`https://wifi.opshome.run/`


## GitHub Pages 子目录部署

本修正版所有本地资源均使用相对路径，可直接部署到 `https://cisco-262.github.io/noc/`，也可部署到 `https://opshome.run/` 根目录。
