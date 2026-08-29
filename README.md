# 来开博客

基于 [Astro](https://astro.build/) 的个人博客（MVP 版本）。

## 功能

- 首页文章列表（按时间倒序）
- 文章详情页（Markdown 渲染 + Shiki 代码高亮，自动适配深色模式）
- RSS 订阅（`/rss.xml`）
- sitemap（`/sitemap-index.xml`）
- 草稿支持：frontmatter 中 `draft: true` 的文章不会出现在首页、RSS 和构建产物中

## 写文章

在 `src/content/blog/` 下新建 Markdown 文件（`.md`）：

```markdown
---
title: 文章标题
description: 一句话摘要
pubDate: 2026-08-29
# draft: true  ← 加上这行表示草稿，不会发布
---

正文使用 Markdown 书写。
```

文件名即 URL：`my-post.md` 对应 `/blog/my-post/`。

## 常用命令

| 命令             | 说明                                     |
| :--------------- | :--------------------------------------- |
| `npm install`    | 安装依赖                                 |
| `npm run dev`    | 启动本地开发服务器（localhost:4321）     |
| `npm test`       | 类型检查（astro check）+ 生产构建        |
| `npm run build`  | 构建生产版本到 `./dist/`                 |
| `npm run preview`| 本地预览构建产物                         |

## 注意事项

- 每次改动完成后，必须创建一个对应的 Git commit，以便追踪和回滚。
- 每次改动后，必须编写或更新相关测试，并在交付给用户前确保所有测试和验证全部通过。
