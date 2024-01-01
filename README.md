# 2024新春版：零基础Docker全栈开发部署速通攻略

精心整理的适合初学者的Docker速成教程。把知识点与实操相结合，把晦涩的概念变得通俗易懂。

教程对每一条命令都做了参数的详细讲解，手把手带你快速扎实基础、掌握实战，节约大量自己学习、摸索、爬坑的时间。

> 源码解压密码，见配套教程原文。

## 配套教程

📚📚本项目有详细的讲解教程，原文请关注我的微信公众号【卧梅又闻花】📚📚

《2024新春版：零基础Docker全栈开发部署速通攻略》

先看下目录了解本教程都有哪些内容。

## 章节目录
```
1 Docker通俗解释
2 安装Docker
• 2.1 Windows安装方法
• 2.2 macOS安装方法
• 2.3 Linux(Ubuntu)安装方法
3 Docker初识篇
• 3.1 Docker基础环境相关命令
• 3.2 初识镜像（Image）和容器（Container）
• 3.3 开篇实战：搭建本地开发环境的Nginx Web服务（docker container）
• 3.3.1 创建并启动Nginx容器
• 3.3.2 容器的查看、停止、运行与删除
• 3.3.3 构建挂载（volume）宿主机Web目录的Nginx容器
• 3.3.4 小技巧：容器批量操作
• 3.3.5 查看容器的输出日志
• 3.3.6 本章知识点小结
4 Docker基础命令
• 4.1 Docker镜像操作（docker image）
• 4.1.1 拉取镜像
• 4.1.2 列出镜像和删除镜像
• 4.1.3 镜像的导出与导入（给离线机器安装）
• 4.2 挂载数据持久化（docker volume）
• 4.3 进入容器内部运行命令（docker container exec）
• 4.4 将容器打包成镜像（docker container commit）
• 4.5 显示容器正在运行的进程（docker container top）
• 4.6 懒人常用Docker命令
• 4.6.1 批量删除未使用的资源
• 4.6.2 容器运行结束后自动销毁该容器
• 4.7 使用--help查看全部docker命令
• 4.8 本章小结
5 Dockerfile
• 5.1 初识Dockerfile（FROM与RUN，docker image build）
• 5.2 ADD与COPY
• 5.3 WORKDIR
• 5.4 ARG与ENV
• 5.5 CMD
• 5.6 ENTRYPOINT
• 5.7 HEALTHCHECK
• 5.8 EXPOSE
• 5.9 VOLUME
• 5.10 更多Dockerfile命令
• 5.11 Dockerfile实战：使用Dockerfile构建静态网站Nginx镜像
• 5.12 本章小结
6 Docker Network
• 6.1 初识Docker Network
• 6.2 查看容器的网络配置（docker container inspect）
• 6.3 常用docker network命令
• 6.4 设置容器的网络
• 6.5 为什么不推荐使用默认名称为bridge的网络
• 6.6 host驱动模式网络
• 6.7 本章小节
7 Docker Compose
• 7.1 初识Docker Compose
• 7.2 安装Docker Compose
• 7.3 compose文件
• 7.4 docker compose常用命令
• 7.5 本章小结
8 全栈综合实战：搭建Nginx+PHP+Nodejs+MySQL全栈工程（开发环境+生产环境）
• 8.1 创建项目专用网络
• 8.2 搭建MySQL数据库
• 8.3 使用Docker版phpmyadmin可视化管理数据库
• 8.4 使用MySQL Workbench可视化管理数据库
• 8.5 搭建Nodejs API服务
• 8.5.1 基于express构建Nodejs项目
• 8.5.2 制作Nodejs服务的Docker镜像
• 8.5.3 运行Nodejs服务容器
• 8.6 搭建PHP API服务
• 8.6.1 安装ThinkPHP
• 8.6.2 实现PHP API业务逻辑
• 8.6.3 配置php.ini
• 8.6.4 基于php-apache制作开发环境的PHP镜像
• 8.6.5 基于php-fpm制作生产环境的PHP镜像
• 8.7 开发前端网站项目
• 8.7.1 基于Vite5初始化React网站项目
• 8.7.2 精简项目
• 8.7.3 支持Sass/Scss/Less/Stylus
• 8.7.4 重构页面
• 8.7.5 配置开发环境反向代理
• 8.7.6 在开发环境运行项目
• 8.7.7 build前端静态化网站项目
• 8.8 搭建生产环境Nginx Web服务
• 8.8.1 配置生产环境Nginx
• 8.8.2 编写dockerfile
• 8.8.3 创建生产环境的Nginx镜像
• 8.9 使用docker compose一气呵成开发环境全栈部署
• 8.10 上传Docker镜像
• 8.11 在生产环境使用docker compose部署全栈项目
• 8.12 其他说明
• 8.12.1 在多个服务器（宿主机）上部署
• 8.12.2 设置服务器开机自动启动项目容器
• 8.12.3 容器日志目录的挂载
• 8.12.4 选择安全的Dockerhub镜像
• 8.12.5 Python/Java/Go/C#/Rust等开发语言的Docker官方指南
9 教程源码及镜像源
结束语
```

## 教程使用的系统环境及软件版本
```
【操作系统】
Windows 11
macOS Sonoma 14
Ubuntu 22.04 64位 UEFI版

【Docker软件】
Docker Engine: 24.0.7
Docker Desktop: 4.26.1
Docker Compose: v2.23.3-desktop.2

【Docker镜像】
mysql: 8.2.0
phpmyadmin: 5.2.1
node: 20.10.0
composer: 2.6.6
php: 8.3.0-apache
php: 8.3.0-fpm

【主要框架包】
express: 4.18.2
mysql2: 3.6.5
topthink/framework (ThinkPHP): 8.0.3
vite: 5.0.8
react: 18.2.0
antd: 5.12.5
```