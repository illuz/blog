+++
title = '博客修整及记录（进行中）'
categories = ["技术"]
tags = ["日常"]
date = 2024-06-05T10:16:37+08:00
draft = false
+++

## 目前待办

- [x] 添加评论功能 Disqus
- [x] favicon
- [x] RSS 全文输出
- [ ] 增加文章搜索
- [x] Google Analytic
- [x] 头部添加文章时间、Tags 展示、Category 展示
- [ ] 添加文章目录 TOC，参考 https://ichochy.com/ 的效果
- [ ] 代码展示效果优化
- [ ] 增加上一篇下一篇
- [ ] 增加相关文章
- [ ] 从 LogSeq 自动同步生成文章过来

## 评论功能 Disqus

Hugo 自带对 Disqus 的支持： https://gohugo.io/content-management/comments/

只要配置一下 hugo.toml 就行了，hyde 主题已经自带了 disqus 了。

```toml
[services]
  [services.disqus]
    shortname = 'your-disqus-shortname'
```

## favicon

随便弄了一个。

## RSS 全文输出

将官方的 rss.xml 覆盖到 layouts/_default/rss.xml，然后在 description 后面加上 content 就行了：

```xml
      <description>{{ .Summary | transform.XMLEscape | safeHTML }}</description>
      <content:encoded>{{ .Content | safeHTML }}</content:encoded>
```

## Google Analytic

按 hyde 主题的 readme 提示配置后没效果，发现新的 Hugo 配置变了，现在得使用下面的配置：

```toml
[services]
  [services.googleAnalytics]
    id = 'G-xxx'
```

## 其它注意点

- 需要将 hasCJKLanguage 设置成 true，否则 summaryLength 会以 word 为单位计算，而不是字符。
