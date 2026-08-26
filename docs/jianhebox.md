# 简盒 JianHeBox 定制版

本页介绍基于本仓库 fork 的 **简盒 JianHeBox** 工具集，以及与上游 BentoPDF 的关系。

## 什么是简盒 JianHeBox？

[简盒 JianHeBox](https://jianhebox.cn) 是一个**5 个 AI 工具合集**（提示词优化、PDF 转 Markdown、Markdown 转 Word、正则测试、Cron 表达式），所有工具**完全免费、100% 客户端运行**、用户 API Key 仅存在本机浏览器。

PDF 转 Markdown 工具是简盒的第 2 款工具，基于 **BentoPDF** 二次开发。

## 简盒的 PDF 工具 vs 上游 BentoPDF

| 维度 | 上游 BentoPDF | 简盒 PDF 工具 |
|---|---|---|
| 协议 | AGPL-3.0 | AGPL-3.0（继承） |
| 来源 | https://github.com/alam00000/bentopdf | https://github.com/colorfulboys/bentopdf |
| 部署 | Cloudflare Pages / 自托管 | Cloudflare Pages（自动部署） |
| 中文 | 内置 zh-CN/zh-TW | 继承上游，更完善 |
| 工具集 | 仅 PDF 工具 | 5 工具合集（PDF + AI 提示词 + ...） |
| 入口 | bentopdf.com | jianhebox.cn |
| 隐私 | 100% 客户端 | 100% 客户端 |

## 简盒 fork 做了什么定制？

1. **品牌化**：页面头部、页脚加 "简盒 JianHeBox" 品牌标识
2. **AGPL-3.0 合规 footer**：保留原作者版权链接 + 协议链接
3. **自动部署**：通过 GitHub Actions 自动 build 并部署到 Cloudflare Pages
4. **SEO 优化**：sitemap.xml、robots.txt、canonical URL
5. **域名绑定**：`pdf.jianhebox.cn`（计划中）

## 简盒的隐私承诺

简盒的所有 AI 工具**绝对**不存储、不上传任何用户数据：

- ✅ **API Key 仅存在 IndexedDB**（你的电脑本地）
- ✅ **无后端服务器**（CF Pages 静态托管）
- ✅ **所有 AI 调用**都是浏览器直连 AI 服务商官方 API
- ✅ **PDF 处理** 100% 在浏览器内（WebAssembly）
- ✅ **不埋任何统计/追踪/广告**

## 简盒的盈利模式

简盒的 5 个工具**永远免费**。站长不烧钱（每用户自配 Key）。盈利靠：

1. **SEO 内容**（jianhebox.cn 已有 20+ 篇深度文章）
2. **联盟营销**（AI 工具推荐分成）
3. **付费工具**（未来 1-2 个垂直工具，月费 9.9-29.9 元）

## 使用 BentoPDF 部署到简盒

如果你想自己 fork 简盒版：

```bash
# 1. Fork
git clone https://github.com/colorfulboys/bentopdf.git
cd bentopdf

# 2. 安装依赖
npm install

# 3. 改品牌（README.md 已示范）
# 修改 title、footer、AGPL-3.0 致谢等

# 4. 构建
npm run build

# 5. 部署到 Cloudflare Pages
# 通过 GitHub Actions 自动部署（见 .github/workflows/）
```

## 联系简盒

- 官网：https://jianhebox.cn
- 备份域名：https://jianhebox.com
- 仓库：https://github.com/colorfulboys/prompt-optimizer
- 反馈：在 https://jianhebox.cn/#/articles 看教程底部留言

## 致谢

感谢 [alam00000](https://github.com/alam00000) 创建 [BentoPDF](https://github.com/alam00000/bentopdf)，简盒的所有 PDF 工具都基于此开源项目。**AGPL-3.0 协议要求保留原作者版权**，简盒严格遵守。
