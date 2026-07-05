# AGENTS.md

## 项目概览

MindRealm - 一个情绪陪伴 AI 聊天界面静态页面。

## 技术栈

- 纯 HTML / CSS / JavaScript (原生极简项目)
- 无构建步骤，无 npm 依赖
- 通过 Python http.server 提供静态文件服务

## 项目结构

```
.
├── index.html    # 主页面（含样式和脚本）
├── .coze         # 项目配置
└── AGENTS.md     # 项目说明
```

## 开发命令

- 启动服务: `python -m http.server ${DEPLOY_RUN_PORT} --bind 0.0.0.0`
- 无需构建或安装依赖

## 核心功能

- 聊天界面：暗色主题，居中卡片布局
- AI 对话：调用 HuggingFace API (google/gemma-2-9b-it 模型)
- 系统提示词：温柔的情绪陪伴 AI，回复控制在 60 字以内

## 注意事项

- API Key 需要替换 `index.html` 中的 `YOUR_HF_TOKEN` 占位符
- API 调用在前端直接发起，适用于个人使用场景
