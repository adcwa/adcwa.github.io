# Jekyll 博客项目 - 完整使用指南

基于 Jekyll 构建的个人博客网站，使用 GitHub Pages 部署。

## 📋 项目概述

- **网站地址**: https://adcwa.github.io
- **技术栈**: Jekyll + GitHub Pages
- **主题**: Minima (Jekyll 默认主题)
- **部署平台**: GitHub Pages
- **文章格式**: Markdown

## 🛠 环境配置

### 1. 安装 Ruby 环境
```bash
# 安装 rbenv (推荐使用 rbenv 管理 Ruby 版本)
brew install rbenv

# 安装 Ruby 3.2.2
rbenv install 3.2.2

# 设置默认 Ruby 版本
rbenv global 3.2.2   # 全局设置
# 或者
rbenv local 3.2.2    # 仅当前目录设置
```

### 2. 安装依赖
```bash
# 安装 bundler 和 jekyll
gem install bundler
gem install jekyll

# 安装项目依赖
bundle install
```

## 🚀 本地开发

### 启动开发服务器
```bash
# 启动 Jekyll 本地服务器
bundle exec jekyll serve

# 带实时重载的启动方式
bundle exec jekyll serve --livereload

# 指定端口
bundle exec jekyll serve --port 4001
```

访问 http://localhost:4000 查看网站

### 构建静态文件
```bash
# 构建网站到 _site 目录
bundle exec jekyll build

# 构建并监听文件变化
bundle exec jekyll build --watch
```

## ✍️ 文章写作

### 1. 创建新文章
在 `_posts` 目录下创建新文件，文件名格式：`YYYY-MM-DD-文章标题.markdown`

例如：`2024-12-20-my-first-post.markdown`

### 2. 文章格式模板
```markdown
---
layout: post
title: "文章标题"
date: 2024-12-20 10:00:00 +0800
categories: [分类1, 分类2]
tags: [标签1, 标签2]
author: 作者名
excerpt: "文章摘要"
---

# 文章标题

这里是文章内容...

## 二级标题

### 三级标题

**粗体文本**

*斜体文本*

- 列表项1
- 列表项2

1. 有序列表1
2. 有序列表2

[链接文本](https://example.com)

![图片描述](图片URL)

```代码块```

> 引用文本
```

### 3. Front Matter 配置

必需字段：
- `layout`: 布局类型 (post, page, default)
- `title`: 文章标题
- `date`: 发布日期

可选字段：
- `categories`: 分类
- `tags`: 标签
- `author`: 作者
- `excerpt`: 摘要
- `permalink`: 自定义URL
- `published`: 是否发布 (false 为草稿)

### 4. 代码高亮
Jekyll 支持多种代码高亮方式：

#### 使用 Liquid 标签
```liquid
{% highlight ruby %}
def hello_world
  puts "Hello, World!"
end
{% endhighlight %}
```

#### 使用 Markdown 代码块
````markdown
```javascript
function helloWorld() {
  console.log("Hello, World!");
}
```
````

## 📄 页面管理

### 创建新页面
在根目录创建 `.markdown` 或 `.md` 文件：

```markdown
---
layout: page
title: 页面标题
permalink: /page-url/
---

页面内容...
```

### 页面布局类型
- `page`: 静态页面布局
- `post`: 文章页面布局
- `home`: 首页布局
- `default`: 默认布局

## 🎨 主题定制

### 1. 修改配置文件
编辑 `_config.yml` 文件：

```yaml
# 网站基本信息
title: 网站标题
email: your-email@example.com
description: 网站描述
baseurl: "/" 
url: "https://yourusername.github.io"

# 作者信息
author:
  name: 你的名字
  email: your-email@example.com
  github: yourusername

# 主题设置
theme: minima
plugins:
  - jekyll-feed
  - jekyll-seo-tag
  - jekyll-sitemap

# Minima 主题配置
minima:
  skin: dark  # 可选: dark, classic, auto
  date_format: "%Y-%m-%d"
  
# 社交媒体链接
social_links:
  github: yourusername
  twitter: yourusername
  linkedin: yourusername
```

### 2. 自定义样式
创建 `_sass` 目录和 `assets/main.scss` 文件：

```scss
---
---

@import "minima";

// 自定义样式
.custom-class {
  color: #333;
  font-size: 18px;
}
```

### 3. 覆盖主题文件
创建 `_layouts`, `_includes`, `_sass` 目录来覆盖主题默认文件。

### 4. 切换主题
在 `_config.yml` 中修改主题：

```yaml
# 使用其他主题
theme: minimal-mistakes-jekyll
# 或
remote_theme: "mmistakes/minimal-mistakes"
```

然后运行：
```bash
bundle install
bundle exec jekyll serve
```

## 🔧 高级功能

### 1. 添加评论系统
使用 Disqus 或 Utterances：

```yaml
# _config.yml
disqus:
  shortname: your-disqus-shortname

# 或使用 Utterances
utterances:
  repo: "username/repo-name"
  issue-term: "pathname"
  theme: "github-light"
```

### 2. 添加搜索功能
使用 Simple-Jekyll-Search：

```html
<!-- _includes/search.html -->
<div id="search-container">
  <input type="text" id="search-input" placeholder="搜索文章...">
  <ul id="results-container"></ul>
</div>

<script src="/assets/js/simple-jekyll-search.min.js"></script>
<script>
  SimpleJekyllSearch({
    searchInput: document.getElementById('search-input'),
    resultsContainer: document.getElementById('results-container'),
    json: '/search.json'
  })
</script>
```

### 3. 添加分析工具
Google Analytics：

```yaml
# _config.yml
google_analytics: UA-NNNNNNNN-N
```

### 4. 添加 RSS 订阅
Jekyll-feed 插件自动生成 RSS：

```yaml
# _config.yml
plugins:
  - jekyll-feed
```

访问 `/feed.xml` 获取 RSS 链接。

### 5. 添加网站地图
```yaml
# _config.yml
plugins:
  - jekyll-sitemap
```

### 6. SEO 优化
```yaml
# _config.yml
plugins:
  - jekyll-seo-tag
```

在 `_layouts/default.html` 中添加：
```html
<head>
  {% seo %}
</head>
```

## 📱 部署指南

### GitHub Pages 自动部署
1. 推送代码到 GitHub 仓库
2. 在仓库设置中启用 GitHub Pages
3. 选择 main 分支作为源
4. 网站将自动部署到 `https://username.github.io`

### 手动部署流程
```bash
# 构建网站
bundle exec jekyll build

# 提交更改
git add .
git commit -m "更新网站内容"
git push origin main
```

## 📝 常用命令

```bash
# 创建新的 Jekyll 站点
jekyll new my-site

# 安装依赖
bundle install

# 更新依赖
bundle update

# 本地预览
bundle exec jekyll serve

# 构建网站
bundle exec jekyll build

# 清理构建文件
bundle exec jekyll clean

# 检查网站健康状态
bundle exec jekyll doctor
```

## 🔍 故障排除

### 常见问题

1. **Ruby 版本不兼容**
   ```bash
   rbenv install 3.2.2
   rbenv global 3.2.2
   ```

2. **Bundler 版本冲突**
   ```bash
   gem install bundler
   bundle install
   ```

3. **端口被占用**
   ```bash
   bundle exec jekyll serve --port 4001
   ```

4. **GitHub Pages 构建失败**
   - 检查 `_config.yml` 语法
   - 确保使用 GitHub Pages 支持的插件
   - 查看 GitHub Actions 构建日志

### 调试技巧
- 使用 `--verbose` 参数查看详细日志
- 检查 `_site` 目录生成的文件
- 使用 `jekyll doctor` 检查问题

## 📚 学习资源

- [Jekyll 官方文档](https://jekyllrb.com/docs/)
- [GitHub Pages 文档](https://docs.github.com/pages)
- [Minima 主题文档](https://github.com/jekyll/minima)
- [Markdown 语法指南](https://www.markdownguide.org/)
- [Liquid 模板语言](https://shopify.github.io/liquid/)

## 📞 联系方式

- 作者: adcwa
- 邮箱: adcwangfeng@gmail.com
- GitHub: [@adcwa](https://github.com/adcwa)

---