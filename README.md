# Kanson's Blog

Hexo 8 + [Volantis](https://github.com/volantis-x/hexo-theme-volantis) 6.8.3，部署在 GitHub Pages：

**<https://kanson1996.github.io/>**

## 分支

- `hexo`：源码（当前分支）
- `master`：`hexo generate` 的静态产物，由 GitHub Pages 提供访问

## 环境

- Node.js 22 LTS（见 `.nvmrc`）
- npm 10+

## 常用命令

```bash
nvm use            # Node 22
npm install
npm run server     # 本地预览 http://localhost:4000
npm run build      # 生成到 public/
npm run deploy     # 生成并推送到 master
```

## 站点说明

- 文章：`source/_posts/`，永久链接保持 `:year/:month/:day/:title/` 不变。
- 主题：`themes/volantis/`（已 vendored，版本 6.8.3），配置覆盖在
  `source/_data/volantis.yml`。
- 统计：Volantis 内置的“新版不蒜子”(penndu / bsz.dusays.com)。为了避免主题里
  重复 ID 只更新第一个元素的问题，使用了 `source/js/bsz.js`（对官方 17.0.0
  脚本的小补丁，会更新所有同名 ID）。
- 字数/阅读时长：`hexo-wordcount` + Volantis 的 `plugins.wordcount`。
- 版权年份：`source/_volantis/bodyEnd.ejs` 在浏览器端更新，跨年无需重新构建。
- 自定义域名 `kanson.net` 已过期，不再使用 CNAME；canonical 为
  `https://kanson1996.github.io`。
- 归档时间线：`source/archives/index.md`（Volantis 的 `layout: archive`）。
