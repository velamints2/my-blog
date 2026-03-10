---
title: 'Astro 博客搭建指南'
description: '详细介绍如何使用 Astro 从零搭建一个现代化的个人博客。'
pubDate: '2026-03-10'
tags: ['Astro', '教程', '前端']
---

## 准备工作

在开始之前，你需要确保安装了以下工具：

- **Node.js** 18 或更高版本
- **npm** 或 **pnpm** 包管理器
- 一个代码编辑器（推荐 VS Code）

## 创建项目

```bash
npm create astro@latest my-blog
```

## 项目结构

```
my-blog/
├── public/          # 静态资源
├── src/
│   ├── components/  # 可复用组件
│   ├── content/     # 内容集合
│   ├── layouts/     # 页面布局
│   ├── pages/       # 路由页面
│   └── styles/      # 样式文件
└── astro.config.mjs # Astro 配置
```

## Content Collections

Astro 的内容集合（Content Collections）让管理博客文章变得非常简单：

```typescript
// src/content.config.ts
import { defineCollection, z } from 'astro:content';

const blog = defineCollection({
  type: 'content',
  schema: z.object({
    title: z.string(),
    description: z.string(),
    pubDate: z.coerce.date(),
    tags: z.array(z.string()).default([]),
  }),
});
```

## 部署

### GitHub Pages

配置 GitHub Actions workflow，每次推送到 `main` 分支时自动构建部署。

### Vercel

只需要在 Vercel 中导入仓库，选择 Astro 框架即可一键部署。

## 总结

Astro 是目前搭建博客的最佳选择之一，它的**内容优先**理念和**出色的性能**让你可以专注于写作本身。
