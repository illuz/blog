+++
title = '博客修整及记录（进行中）'
date = 2024-06-05T10:16:37+08:00
draft = true
+++

## 目前待办

- [x] 添加评论功能 Disqus
- [x] favicon
- [ ] 增加 RSS
- [ ] 增加文章搜索
- [ ] Google Analytic
- [ ] 头部添加文章时间、Tags 展示、Category 展示
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

## Google Analytic

