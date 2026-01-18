# 🌟 AI-AllInOne API 中转站
一个接口聚合 100+ 主流 AI 大模型，统一接入、成本直降，让 AI 调用更高效便捷！

[![GitHub stars](https://img.shields.io/github/stars/你的用户名/仓库名?style=social)](https://github.com/pclark-582c9/OpenAPI-Freeapi/stargazers)

## 📌 核心优势
- **多模聚合**：覆盖通义千问、文心一言、GLM、Deepseek 等 100+ 主流 AI 模型，无需逐个对接
- **成本极低**：调用成本仅为官方平台的 1/8，大幅降低 AI 开发与使用成本
- **统一接口**：标准化 API 格式，切换模型无需修改代码，提升开发效率
- **快速接入**：极简配置流程，注册即可获取密钥，分钟级上手使用

## 🚀 快速开始
### 1. 获取 API 密钥
访问官方网站注册账号，即可免费获取专属 API 密钥：[https://zypwtohm.ap-northeast-1.clawcloudrun.com/](https://zypwtohm.ap-northeast-1.clawcloudrun.com/)

### 2. 调用示例（JavaScript）
```javascript
// 发送请求到统一 API 地址
fetch('https://zypwtohm.ap-northeast-1.clawcloudrun.com/v1/chat/completions', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
    'Authorization': 'Bearer 你的API密钥' // 替换为注册后获取的密钥
  },
  body: JSON.stringify({
    model: 'openai/gpt-oss-20b', // 支持切换其他模型（如 tongyi/qwen-max、ernie-bot 等）
    messages: [
      { role: 'user', content: '你好，请介绍一下你自己' }
    ]
  })
})
.then(response => response.json())
.then(data => console.log(data.choices[0].message.content));
