---
title: Markdown 与代码高亮测试
description: 用于验证 Markdown 渲染与 Shiki 代码高亮的测试文章，同时演示草稿机制之外的全部排版元素。
pubDate: 2026-08-20
tags:
  - Markdown
---

这篇文章用来验证 MVP 的 Markdown 渲染与代码高亮是否正常。

## 行内与块级元素

行内元素：**加粗**、*斜体*、`行内代码`、[链接](https://astro.build/)。

> 这是一段引用文本，用来验证引用样式的展示效果。

### 代码块

```typescript
interface Post {
  title: string;
  pubDate: Date;
}

function formatDate(post: Post): string {
  return post.pubDate.toLocaleDateString('zh-CN');
}
```

```python
def greet(name: str) -> str:
    return f"Hello, {name}!"
```

## 列表

1. 第一项
2. 第二项
   - 嵌套项
   - 另一个嵌套项

| 表头一 | 表头二 |
| ------ | ------ |
| 单元格 | 单元格 |
| 单元格 | 单元格 |

---

以上。如果这段文字渲染正常，说明文章详情页工作正常。
