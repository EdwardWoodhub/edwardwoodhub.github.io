---
title: 自托管程序
full_width: true
---


以下是常见自托管程序的分类（按「本机 Docker 服务端 + 浏览器访问」模式）：

### 主动按这种模式设计的程序

这些项目从一开始就以 **Docker / 容器部署 + Web 界面** 作为主要（甚至唯一）使用方式。

| 程序 | 类别 | 说明 |
|------|------|------|
| **Audiobookshelf** |	有声书/播客 |	专为自托管设计的有声书服务器，完全围绕 Docker 和 Web/移动端构建，进度云端同步 |
| **Ayakaleaf Pro** | LaTeX 协作编辑 | Overleaf Community Edition 的开源增强版，官方主推 Docker 部署，浏览器访问的在线协作编辑器 |		
| **Home Assistant** | 智能家居 | 容器/OS 部署非常主流，Web/移动端控制 |		
| **Homepage / Dashy** |	导航看板 |	Homelab 玩家标配，通过 YAML 配置的纯 Web 仪表盘，专门通过容器一键部署 |
| **Immich** | 照片管理 | 官方主推 Docker，Web + 移动端为主 |		
| **Jellyfin** | 媒体服务器 | 核心是服务端，Web 是主要访问方式之一 |		
| **Kasm Workspaces** |	容器化云桌面 |	致力于将浏览器直接转化为“云操作系统”，天生为容器隔离和 Web 界面串流设计 |
| **Mealie** |	食谱与膳食管理 |	纯 Web 架构的本地食谱管理器，前后端分离，官方强烈建议通过 Docker 部署 |
| **n8n** | 自动化工作流 | 官方推荐 Docker，界面完全是 Web |		
| **Nextcloud** | 文件同步/协作 | Web 优先，Docker 是主流部署方式之一 |		
| **Outline** |	团队知识库 |	现代化的在线 Wiki，深度依赖 Docker 和 OIDC 单点登录，界面体验媲美 Notion |
| **Paperless-ngx** | 文档管理 | 设计之初就是 Web 应用 + Docker |		
| **Plausible / Umami** | 网站分析 | 隐私友好分析工具，Docker 部署为主 |		
| **Stirling-PDF** |	PDF 处理 |	纯 Web 界面的 PDF 工具瑞士军刀（拆分、合并、OCR），官方主推 Docker 部署 |
| **Uptime Kuma** | 监控 | 轻量 Web 应用，Docker 一键部署 |		
| **Vaultwarden** | 密码管理 | Bitwarden 兼容实现，主形态是自托管 Web 服务 |		
| **Wiki.js** | Wiki | Web 应用，Docker 官方支持良好 |		
		
		
		


### 不是这样设计，但可以这样做的程序

这些程序原本有其他形态（原生客户端、传统安装方式等），但提供了官方或社区 Docker 镜像，并且有 Web 界面，可以按同样方式使用。

| 程序 | 类别 | 说明 |
|------|------|------|
| **BookStack** | Wiki/文档 | 有传统安装方式，Docker 也很成熟 |		
| **Calibre-Web** |	电子书库 |	依托传统桌面端 Calibre 笨重的本地数据库，为其套上一层专为浏览器阅读和共享设计的现代化 Web 外壳 |
| **Code-Server** | 开发环境 | VS Code 的 Web 版，本质就是服务端 + 浏览器 |		
| **Gitea / Forgejo** | Git 托管 | 有传统安装，但 Docker 非常常用，界面是 Web |		
| **Grafana** | 监控仪表盘 | 有多种部署方式，Docker 是常见选择 |		
| **Jellyfin** | 媒体服务器 | 也有各类原生客户端，但 Web 访问完全可用 |		
| **JupyterLab** |	科学计算环境 |	核心是本地计算引擎（可接入 Python 或 Wolfram Engine），通过容器化和 Web 界面完美转化为云端科研 IDE |
| **linuxserver/webtop** |	桌面环境 |	将传统的 Linux 桌面（如 Alpine, Arch, Ubuntu）打包进容器，通过 KasmVNC 纯浏览器输出 GUI，实现“伪云端 OS”体验 |
| **MATLAB** |	数值计算与可视化 |	传统的重型桌面软件。如今不仅有官方 Docker 支持，还可通过 mpm (MATLAB Package Manager) 定制工具箱。通过集成 matlab-proxy，能够直接在浏览器中渲染原生 X11 GUI 界面，将极高负载的矩阵或张量运算完全下放到服务器。 |
| **PhotoPrism** |	照片管理 |	核心是本地照片索引和 AI 标签引擎，虽有部分桌面端同步工具，但交互完全依赖以 Docker 驱动的 Web 界面 |
| **Plex** | 媒体服务器 | 有官方 Docker，但更偏商业生态，也有原生客户端 |		
| **Portainer / Dockge** | 容器管理 | 本身就是管理 Docker 的 Web UI |		
| **qBittorrent** |	下载工具 |	经典的桌面端 P2P 软件，但其“无头模式 (Headless)” + Docker + Web UI 的形态在 NAS 和 VPS 圈是绝对主流 |
| **Syncthing** |	文件同步 |	本质是底层的 P2P 同步守护进程（也有原生客户端），但在服务器端，Docker 部署并完全依赖 Web GUI 管理是标准姿势 |
| **Trilium Notes** | 笔记 | 有桌面客户端，同时支持服务器模式 + Web |		
| **Wolfram Engine** |	符号计算与建模 |	核心是本地独立运行的数学引擎与笔记本前端。官方虽然没有直接提供开箱即用的完整 Web GUI Docker 镜像，但可以通过将其引擎容器化，结合 JupyterLab (通过 WolframLanguageForJupyter 插件) 提供浏览器界面，实现架构上的前后端分离。 |
		
		
		
		
		
		
		
		


**简要区分**：

- **主动设计**：项目文档和社区默认就推荐 Docker + 浏览器，几乎没有「必须装原生桌面客户端」的假设。
- **可以这样做**：有 Web 界面和 Docker 支持，但项目也维护原生客户端或其他安装方式，用户可以选择。

