# dsyou-content

shiyou 的博客文章内容仓库。

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

## 文章支持的功能

- **文字格式**：`**加粗**`、`*斜体*`、`~~删除线~~`、`[链接](https://...)`
- **列表、引用、表格、代码块**（自动高亮）
- **数学公式**（KaTeX）：行内 `$E = mc^2$`，块级 `$$...$$`
- **提示框**：
  ```
  > [!TIP]
  > 这是提示框
  ```
  支持 `NOTE` / `TIP` / `IMPORTANT` / `WARNING` / `CAUTION`
- **图片**：图片放进 `blog/images/`，正文用相对路径引用：
  ```mdx
  ![图片说明](./images/xxx.jpg)
  ```
- **嵌入视频**：直接写 iframe HTML（YouTube / B 站都支持）

## 目录结构

```
dsyou-content/
├── blog/
│   ├── 我的文章.mdx
│   └── images/
│       └── xxx.jpg    ← 文章图片放这里
└── .github/workflows/  ← 自动部署用的 Action（一般不用动）
```

## 注意事项

- 每篇文章一个 `.mdx` 文件，文件名就是文章 URL（如 `hello-world.mdx` → `/blog/hello-world`）
- `publishedAt` 用 `YYYY-MM-DD` 格式
- `tags` 用英文逗号或中文逗号分隔多个标签
- 删除文章 = 删除对应文件并推送

