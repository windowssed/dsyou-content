# dsyou-content

windowssed 的博客文章内容仓库。

`blog` 文件夹里的 `.mdx` 文件就是网站 `https://www.dsyou.cn` 显示的文章。网站构建时会自动从这里拉取最新内容。

## 如何添加新文章

在 `blog` 文件夹新建一个 `.mdx` 文件，格式如下：

```mdx
---
title: "文章标题"
publishedAt: "2026-08-06"
summary: "文章简介"
tags: "标签1, 标签2"
---

这里是文章正文，支持 Markdown 语法。
```

推送到本仓库后，网站会自动重新构建并上线新文章。
