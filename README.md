# My Personal Blog

基于 [Astro](https://astro.build) 构建的个人博客。

## 🚀 项目结构

```
├── public/              # 静态资源
├── src/
│   ├── components/      # 组件
│   ├── content/blog/    # 博客文章 (Markdown/MDX)
│   ├── layouts/         # 页面布局
│   ├── pages/           # 页面路由
│   └── styles/          # 全局样式
├── astro.config.mjs     # Astro 配置
└── package.json
```

## 📝 使用方法

### 开发
```bash
npm run dev
```

### 构建
```bash
npm run build
```

### 预览构建结果
```bash
npm run preview
```

## ✍️ 写文章

在 `src/content/blog/` 目录下新建 `.md` 或 `.mdx` 文件：

```markdown
---
title: "文章标题"
description: "文章描述"
pubDate: "2026-03-11"
tags: ["标签1", "标签2"]
---

正文内容...
```

## 🚀 部署

### GitHub Pages
项目已配置 GitHub Actions 自动部署，推送到 `main` 分支即可自动构建部署。

### Vercel
1. 在 [Vercel](https://vercel.com) 导入 GitHub 仓库
2. 框架选择 Astro
3. 点击部署即可

## 📄 License

MIT
