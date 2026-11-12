---
title: 自托管程序
full_width: true
---


以下是常见自托管程序的分类（按「本机 Docker 服务端 + 浏览器访问」模式）：

### 主动按这种模式设计的程序

这些项目从一开始就以 **Docker / 容器部署 + Web 界面** 作为主要（甚至唯一）使用方式。

| 程序 | 类别 | 说明 |
|------|------|------|
| **Ayakaleaf Pro** | LaTeX 协作编辑 | Overleaf Community Edition 的开源增强版，官方主推 Docker 部署，浏览器访问的在线协作编辑器 |
| **Immich** | 照片管理 | 官方主推 Docker，Web + 移动端为主 |
| **Paperless-ngx** | 文档管理 | 设计之初就是 Web 应用 + Docker |
| **n8n** | 自动化工作流 | 官方推荐 Docker，界面完全是 Web |
| **Uptime Kuma** | 监控 | 轻量 Web 应用，Docker 一键部署 |
| **Vaultwarden** | 密码管理 | Bitwarden 兼容实现，主形态是自托管 Web 服务 |
| **Nextcloud** | 文件同步/协作 | Web 优先，Docker 是主流部署方式之一 |
| **Jellyfin** | 媒体服务器 | 核心是服务端，Web 是主要访问方式之一 |
| **Home Assistant** | 智能家居 | 容器/OS 部署非常主流，Web/移动端控制 |
| **Wiki.js** | Wiki | Web 应用，Docker 官方支持良好 |
| **Plausible / Umami** | 网站分析 | 隐私友好分析工具，Docker 部署为主 |

### 不是这样设计，但可以这样做的程序

这些程序原本有其他形态（原生客户端、传统安装方式等），但提供了官方或社区 Docker 镜像，并且有 Web 界面，可以按同样方式使用。

| 程序 | 类别 | 说明 |
|------|------|------|
| **Jellyfin** | 媒体服务器 | 也有各类原生客户端，但 Web 访问完全可用 |
| **Plex** | 媒体服务器 | 有官方 Docker，但更偏商业生态，也有原生客户端 |
| **BookStack** | Wiki/文档 | 有传统安装方式，Docker 也很成熟 |
| **Trilium Notes** | 笔记 | 有桌面客户端，同时支持服务器模式 + Web |
| **Code-Server** | 开发环境 | VS Code 的 Web 版，本质就是服务端 + 浏览器 |
| **Gitea / Forgejo** | Git 托管 | 有传统安装，但 Docker 非常常用，界面是 Web |
| **Grafana** | 监控仪表盘 | 有多种部署方式，Docker 是常见选择 |
| **Portainer / Dockge** | 容器管理 | 本身就是管理 Docker 的 Web UI |

**简要区分**：

- **主动设计**：项目文档和社区默认就推荐 Docker + 浏览器，几乎没有「必须装原生桌面客户端」的假设。
- **可以这样做**：有 Web 界面和 Docker 支持，但项目也维护原生客户端或其他安装方式，用户可以选择。

