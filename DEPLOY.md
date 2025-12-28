# Git 部署指南

按照以下步骤将主题上传到 GitHub 和 Gitee。

## 准备工作

确保你已经安装了 Git，并且配置了用户信息：

```bash
git config --global user.name "你的用户名"
git config --global user.email "你的邮箱"
```

## 步骤 1：进入主题目录

```bash
cd d:\Documents\ObsidianPluginDeveloping\themes\redefine
```

## 步骤 2：初始化 Git 仓库

```bash
git init
```

## 步骤 3：添加所有文件

```bash
git add .
```

## 步骤 4：提交更改

```bash
git commit -m "Initial commit: hexo-theme-redefine-mini v1.0.0"
```

## 步骤 5：添加远程仓库

### 添加 GitHub 仓库

```bash
git remote add github https://github.com/Tlyer233/hexo-theme-redefine-mini.git
```

### 添加 Gitee 仓库

```bash
git remote add gitee https://gitee.com/twilight-and-morning-mist/hexo-theme-redefine-mini.git
```

## 步骤 6：推送到远程仓库

### 推送到 GitHub

```bash
git branch -M main
git push -u github main
```

### 推送到 Gitee

```bash
git push -u gitee main
```

## 一键执行脚本

如果你想一次性执行所有命令，可以使用以下脚本：

### Windows PowerShell

```powershell
cd "d:\Documents\ObsidianPluginDeveloping\themes\redefine"
git init
git add .
git commit -m "Initial commit: hexo-theme-redefine-mini v1.0.0"
git remote add github https://github.com/Tlyer233/hexo-theme-redefine-mini.git
git remote add gitee https://gitee.com/twilight-and-morning-mist/hexo-theme-redefine-mini.git
git branch -M main
git push -u github main
git push -u gitee main
```

### Linux/Mac

```bash
cd ~/Documents/ObsidianPluginDeveloping/themes/redefine
git init
git add .
git commit -m "Initial commit: hexo-theme-redefine-mini v1.0.0"
git remote add github https://github.com/Tlyer233/hexo-theme-redefine-mini.git
git remote add gitee https://gitee.com/twilight-and-morning-mist/hexo-theme-redefine-mini.git
git branch -M main
git push -u github main
git push -u gitee main
```

## 后续更新

当你对主题进行更新后，使用以下命令推送更新：

```bash
git add .
git commit -m "描述你的更新内容"
git push github main
git push gitee main
```

## 创建版本标签（可选）

为重要版本创建标签：

```bash
git tag -a v1.0.0 -m "Release version 1.0.0"
git push github --tags
git push gitee --tags
```

## 常见问题

### 1. 如果远程仓库已存在内容

```bash
git pull github main --allow-unrelated-histories
git pull gitee main --allow-unrelated-histories
```

### 2. 强制推送（谨慎使用）

```bash
git push -f github main
git push -f gitee main
```

### 3. 查看远程仓库

```bash
git remote -v
```

### 4. 修改远程仓库地址

```bash
git remote set-url github https://github.com/Tlyer233/hexo-theme-redefine-mini.git
git remote set-url gitee https://gitee.com/twilight-and-morning-mist/hexo-theme-redefine-mini.git
```

## 完成！

主题已成功上传到 GitHub 和 Gitee。你可以访问以下地址查看：

- GitHub: https://github.com/Tlyer233/hexo-theme-redefine-mini
- Gitee: https://gitee.com/twilight-and-morning-mist/hexo-theme-redefine-mini
