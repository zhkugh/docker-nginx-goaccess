### 项目介绍: Docker-Nginx-GoAccess

#### 概述

Docker-Nginx-GoAccess 是一个结合使用 Docker 容器化技术和 Nginx Web 服务器与实时访问日志分析工具 GoAccess 的项目。它的主要目标是通过容器化的方式快速部署和管理一个具有实时访问统计功能的 Web 服务器环境。

#### 组件及功能

1. **Nginx**:
   - **作用**：作为 Web 服务器，处理和响应 HTTP 请求。
   - **特点**：轻量、高性能、模块化，是常用的静态内容和反向代理服务器。

2. **GoAccess**:
   - **作用**：实时的、交互式的访问日志分析工具。
   - **特点**：
     - 提供实时监控和分析 Web 服务器的访问情况。
     - 支持多种日志格式，包括常见的 Combined Log Format。
     - 可通过 WebSocket 实时更新分析结果，以可视化的方式展示访问数据。

3. **Docker**:
   - **作用**：容器化平台，用于封装、分发和运行应用程序。
   - **特点**：
     - 提供了轻量级的虚拟化技术，实现了环境的一致性和隔离性。
     - 使用 Docker Compose 管理多个容器组成的应用服务，简化了部署和扩展。

#### 使用流程

1. **准备工作**：
   - 安装 Docker 和 Docker Compose。
   - 编写好 Nginx 的配置文件 `nginx.conf`，准备好 GoAccess 配置和报告目录。

2. **编写 Docker Compose 文件**：
   - 定义两个服务：Nginx 和 GoAccess。
   - 配置它们的容器映像、端口映射、数据卷挂载等。

3. **启动服务**：
   - 在项目根目录执行 `docker-compose up -d` 启动服务。
   - Docker Compose 将会创建并启动 Nginx 和 GoAccess 两个容器。

4. **访问 Web 页面**：
   - 打开浏览器访问 `http://localhost` 查看 Nginx 提供的静态内容。
   - 访问 `http://localhost/goaccess/` 查看实时的访问统计报告。

5. **监控和管理**：
   - 使用 Docker 相关命令（如 `docker ps`、`docker logs` 等）监控和管理容器的运行状态和日志输出。

## 优化和扩展

在基础上，可以根据实际需求优化 Nginx 和 GoAccess 的配置，添加 HTTPS 支持、自定义错误页面等功能。通过 Docker 的灵活性，可以快速部署和扩展整个应用环境，以满足不同规模和需求的项目要求。