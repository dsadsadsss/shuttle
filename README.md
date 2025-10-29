# Shuttle 部署指南

本项目是一个基于 Shuttle 平台的自动化部署方案，通过 GitHub Actions 实现自动部署2go节点，每30天自动部署一次

## 部署流程
1. Fork 本项目

2. 注册 [Shuttle](https://www.shuttle.rs/) 账号并获取 API 密钥
<img width="600" height="400" alt="image" src="https://github.com/user-attachments/assets/054f390b-7bfd-4920-8486-6750ab3ace9b" />

3. 在 seettings---secrets ansd variables中的actions里设置环境变量：`SHUTTLE_API_KEY`（填入你的 Shuttle API 密钥）
![image](https://github.com/user-attachments/assets/d67ab79b-8d1d-437e-8c6b-786163e197a2)

其他环境变量可选：NSERVER、NKEY、DOM、TOK、UUID、SUB_NAME、SUB_URL

注意：使用固定隧道token需要在cf后台设置8001

4. actions会自动部署，安装环境时间稍长，预计部署时间需要10分钟，请耐心等待，在actions中查看进度

## 节点获取

方法1 日志复制链接

方法2 部署订阅服务器 https://github.com/dsadsadsss/workers-sub-for-wanju.git，填入SUB_URL

方法3 设置TG参数，节点上传TG

具体可以参考玩具脚本https://github.com/dsadsadsss/java-wanju.git，可以根据需要设置参数
