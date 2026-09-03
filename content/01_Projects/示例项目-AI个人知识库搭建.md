---
title: 示例项目：AI个人知识库搭建
tags: [project, AI, AnythingLLM, DeepSeek]
start_date: 2026-09-04
deadline: 2026-09-10
status: in-progress
---

# 🎯 项目：AI 个人知识库搭建与落地

## 1. 项目目标与交付物
- [x] 安装并启动轻量容器环境 OrbStack。
- [x] 编写 Docker Compose 并在本地部署 AnythingLLM 服务。
- [x] 将 Obsidian 笔记库安全挂载至知识库容器。
- [ ] 接入 DeepSeek API Key 并选定 `deepseek-chat`。
- [ ] 在 AnythingLLM 中建立首次向量索引（Embed）。
- [ ] 尝试首轮个人笔记问答测试。

## 2. 核心架构与参数
- **知识库容器端口**：`3001`
- **向量数据库**：LanceDB（容器内自嵌）
- **Embedding 向量模型**：AnythingLLM 内置 Embedder（免费离线）
- **生成大模型**：DeepSeek-V3 (`deepseek-chat`)

## 3. 遇到的问题与解决记录
- **问题**：Docker Hub 默认镜像源因网络偶发 Bad Gateway。
- **解决**：配置了国内镜像节点 `docker.m.daocloud.io` 并成功拉取镜像。
