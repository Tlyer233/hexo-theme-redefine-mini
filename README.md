# Hexo Theme Redefine Mini

一个基于 [hexo-theme-redefine](https://github.com/EvanNotFound/hexo-theme-redefine) 的定制版主题，专注于简洁、高效的博客体验。

## ✨ 主要特性

在原版 Redefine 主题基础上，增加了以下特性：

### 🎨 界面优化
- ✅ **移除顶部导航栏**：更加简洁的阅读界面
- ✅ **侧边栏目录树**：支持展开/折叠的树形文章导航
- ✅ **当前文章高亮**：自动定位并高亮显示当前阅读的文章
- ✅ **网站标题可点击**：侧边栏标题可跳转回首页
- ✅ **搜索图标优化**：在首页 Banner 和侧边栏添加搜索入口

### 📝 文章功能增强
- ✅ **可调节大纲宽度**：通过拖拽调整右侧大纲栏宽度
- ✅ **智能隐藏**：大纲栏拖拽到阈值自动隐藏
- ✅ **宽度记忆**：自动保存用户调整的大纲宽度
- ✅ **状态同步**：大纲显示/隐藏状态完全同步

### 🎯 用户体验
- ✅ **自然排序**：文章列表支持数字自然排序（1, 2, 3...）
- ✅ **自动滚动**：打开文章时自动滚动到当前位置
- ✅ **响应式设计**：在移动端和平板上保持良好体验

## 🚀 快速开始
### STEP0. 安装
```bash
cd your-hexo-site
git clone https://github.com/Tlyer233/hexo-theme-redefine-mini.git themes/redefine-mini
```

或使用 Gitee：

```bash
git clone https://gitee.com/twilight-and-morning-mist/hexo-theme-redefine-mini.git themes/redefine-mini
```
### STEP1. 修改站点配置

编辑 Hexo 站点根目录的 `_config.yml`：

```yaml
theme: redefine-mini
```

### STEP2. 安装依赖

```bash
npm install hexo-renderer-stylus --save
```

### STEP3. 创建主题配置文件

复制主题配置文件到站点根目录：

```bash
cp themes/redefine-mini/_config.yml _config.redefine-mini.yml
```

### 4. 配置主题

主题已包含完整的默认配置，可以直接使用。如需自定义，编辑 `_config.redefine-mini.yml`：

```yaml
# 站点信息
info:
  title: 曦's Blog
  subtitle: 你居然找到了这!
  author: 明廷盛
  url: https://blog.20040424.xyz

# 图片配置
defaults:
  favicon: https://20040424.xyz/%E5%9C%86%E8%A7%92.png
  avatar: https://20040424.xyz/%E5%9C%86%E8%A7%92.png

# 主题色
colors:
  primary: "#A31F34"
  default_mode: light # light 或 dark

# 首页 Banner
home_banner:
  enable: true
  style: fixed # static 或 fixed
  image: 
    light: https://20040424.xyz/PicList/light.png
    dark: https://20040424.xyz/PicList/dark2.jpg
  title: 曦's Blog
  subtitle:
    text: ['当认为变得"优秀"才配和她在一起时, 就已经不可能和TA在一起了']
    hitokoto:
      enable: true
      show_author: false
  text_color:
    light: "#d5618b"
    dark: "#D1C1C3"
  social_links:
    enable: true
    style: default # default, reverse, center
    links:
      github: https://github.com/Tlyer233
      gitee: https://gitee.com/twilight-and-morning-mist
    qrs:
      weixin: https://20040424.xyz/PicList/20250215102727210.jpg
      qq: https://20040424.xyz/PicList/20250215103005340.jpg
  
# 侧边栏
home:
  sidebar:
    enable: true
    position: left  # left 或 right
    announcement: 📝 文章列表
    links: true

# 搜索
navbar:
  search:
    enable: true
    preload: true

# 文章大纲
articles:
  toc:
    enable: true
```

### 5. 生成并预览

```bash
hexo clean
hexo generate
hexo server
```

访问 `http://localhost:4000` 查看效果。

## 📖 详细配置

### 侧边栏目录树

主题会自动根据文章的分类生成树形目录结构：

```
📁 主分类
  📁 子分类
    📄 文章1
    📄 文章2
  📄 文章3
```

文章需要设置分类（categories）才会出现在侧边栏：

```yaml
---
title: 文章标题
categories:
  - 主分类
  - 子分类
---
```

### 大纲栏调整

文章页面右侧的大纲栏支持：
- 🖱️ **拖拽调整宽度**：鼠标悬停在大纲栏左边缘，出现拖拽光标时可以左右拖动
- 💾 **自动保存**：调整的宽度会自动保存，刷新页面后保持
- 👁️ **自动隐藏**：拖拽到很窄时会自动隐藏，可通过右下角按钮恢复

### Banner 搜索图标

首页 Banner 底部会显示搜索图标（需要在配置中启用搜索功能）：

```yaml
navbar:
  search:
    enable: true
```

## 📄 许可证

本主题基于 [GPL-3.0](LICENSE) 许可证开源。

## 🙏 致谢

本主题基于 [hexo-theme-redefine](https://github.com/EvanNotFound/hexo-theme-redefine) 开发，感谢原作者 [EvanNotFound](https://github.com/EvanNotFound) 的优秀工作。

⭐ 如果这个主题对你有帮助，欢迎给个 Star！
