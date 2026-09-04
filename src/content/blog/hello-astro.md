---
title: 博客第一篇：用 Astro 搭了一个博客
description: 为什么要写博客、为什么选 Astro，以及这个 MVP 版本包含哪些功能。
pubDate: 2026-08-29
tags:
  - Astro
  - 随笔
---

这是这个博客的第一篇文章。网站目前是一个 MVP 版本，只保留了博客最核心的东西：写文章、发出去、被读到。

## 为什么选 Astro

[Astro](https://astro.build/) 是一个面向内容站点的 Web 框架，特点很契合个人博客：

- **默认零 JavaScript**：页面在构建时渲染成静态 HTML，加载快，SEO 友好。
- **Markdown 优先**：文章就是 `.md` 文件，写完 commit 即发布。
- **保留扩展能力**：需要交互时可以按岛屿（Islands）按需引入组件。

## 当前版本包含什么

- 首页文章列表（按时间倒序）
- 文章详情页（Markdown 渲染 + 代码高亮）
- RSS 订阅（`/rss.xml`）
- 草稿支持：frontmatter 里写 `draft: true` 的文章不会发布

## 写作方式

在 `src/content/blog/` 下新建一个 Markdown 文件：

```markdown
---
title: 文章标题
description: 一句话摘要
pubDate: 2026-08-29
---

正文使用 Markdown 书写……
```

commit 并部署之后，文章就上线了。

> 代码块支持语法高亮，比如上面这段。

后续计划：等文章多起来，再加标签/归档和评论（giscus）。欢迎通过 RSS 订阅更新。
