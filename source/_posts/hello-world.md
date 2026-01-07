---
title: Hexo博客搭建-从零开始
date: 2026-01-01 00:00:00
tags: 
  - Hexo
  - 建站
  - 教程
categories: 
  - 技术折腾
---

欢迎来到我的博客！

这是我的第一篇文章。既然你看到了这里，说明我已经成功使用 [Hexo](https://hexo.io/zh-cn/) 搭建起了这个静态博客系统。

在这篇文章中，我将记录从零开始学习 Hexo 的常用指令和基础操作。这既是我的个人备忘录，希望能帮助到同样想搭建个人博客的朋友。

## 什么是 Hexo？

Hexo 是一个快速、简洁且高效的博客框架。它基于 Node.js，可以将 Markdown 文件极速解析成静态的 HTML 页面。

**核心优势：**

* **速度快**：生成静态页面，访问速度极快。
* **支持 Markdown**：我们可以专注于写作，而不用操心复杂的后台逻辑。
* **一键部署**：通过指令即可部署到 GitHub Pages 等平台。

---

## 操作指南 (Quick Start)

搭建 Hexo 博客主要分为以下几个步骤：

### 1. 配置环境

一个好环境是成功的一半，我们需要先安装必要的运行环境。

#### 安装 Node.js
Hexo 基于 Node.js 运行。请前往 [Node.js 官方网站](https://nodejs.org/) 下载并安装 LTS（长期支持）版本。
> 安装完成后，可在终端输入 `node -v` 检查是否安装成功。

#### 安装 Git
Git 是一个分布式版本控制系统，用于管理代码版本及推送到远程仓库。请前往 [Git 官方网站](https://git-scm.com/) 下载并安装。
> 安装完成后，可在终端输入 `git --version` 检查是否安装成功。

### 2. 安装 Hexo CLI

环境配置好后，我们需要安装 Hexo 的全局命令行工具。在命令行（CMD/Terminal/PowerShell）中输入：

```bash
$ npm install -g hexo-cli
```

### 3. 初始化项目

在命令行中输入以下命令来创建一个新的 Hexo 项目文件夹，并自动下载所需文件：

```bash
# 初始化一个名为 my-blog 的文件夹
$ hexo init my-blog
# 进入该文件夹
$ cd my_blog
# 关键步骤：安装项目依赖
$ npm install
```

这将创建一个名为 `my_blog` 的文件夹，并在其中初始化一个新的 Hexo 项目。**请注意，`npm install` 是必须的，否则后续命令无法运行。**

### 4. 常用操作指令

以下是 Hexo 写作和维护中最常用的指令，建议熟记。

#### 新建文章 (New Post)
当你想要写一篇新博客时：

```bash
$ hexo new "我的第二篇文章"
# 或者简写: hexo n "我的第二篇文章"
```
> 生成的文件位于 `source/_posts/` 目录下。

#### 启动本地预览 (Server)
在发布之前，我们通常需要在本地查看效果：

```bash
$ hexo server
# 或者简写: hexo s
```
> 启动后，访问 `http://localhost:4000` 即可预览博客。

#### 清理缓存 (Clean)
如果修改了配置或更换了主题，页面没有更新，建议先清理缓存：

```bash
$ hexo clean
```
> 该命令会清除缓存文件 (`db.json`) 和已生成的静态文件 (`public`)。

#### 生成静态文件 (Generate)
将 Markdown 文件渲染成静态 HTML 页面（生成的文件位于 `public` 文件夹）：

```bash
$ hexo generate
# 或者简写: hexo g
```

> 更多信息：[生成器文档](https://hexo.io/zh-cn/docs/generating.html)

### 5. 部署到远程站点 (Deploy)

将生成的静态网站推送到 GitHub Pages 或其他服务器。在此之前，请确保你已经在 `_config.yml` 中配置好了 `deploy` 选项。

```bash
$ hexo deploy
# 或者简写: hexo d
```

**组合拳小技巧：**
通常我们会使用组合命令来完成“清理 -> 生成 -> 部署”的一条龙操作：
```bash
$ hexo clean && hexo g -d
```

> 更多信息：[部署文档](https://hexo.io/zh-cn/docs/one-command-deployment.html)

---

## 遇到问题？

如果在通过 Hexo 建站过程中遇到问题，可以参考以下资源：

*   **文档**：[Hexo 官方文档](https://hexo.io/zh-cn/docs/) —— 最权威的指南。
*   **常见问题**：[故障排除](https://hexo.io/zh-cn/docs/troubleshooting.html) —— 解决报错的第一站。
*   **GitHub**：[Hexo Issues](https://github.com/hexojs/hexo/issues) —— 看看别人是否遇到过同样的问题。

希望这篇文章能帮你开启愉快的博客之旅！
```