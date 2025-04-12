# SSE Merge View

一个简单但实用的工具，用于合并和格式化 Server-Sent Events (SSE) 响应数据。特别适用于处理 OpenAI 等流式 API 响应的查看和调试。

## 特性

- 🚀 自动合并多个 SSE 事件
- 📝 保留完整的 JSON 结构
- 🎯 自动触发合并，实时预览
- 📋 一键复制结果
- 🌈 美观的用户界面
- 💻 纯前端实现，无需后端服务

## 在线使用

访问：https://100apps.github.io/online-sse-merge-view/

## 本地使用

1. 克隆仓库：
```bash
git clone https://github.com/100apps/online-sse-merge-view.git
```

2. 直接在浏览器中打开 `index.html` 文件即可使用

## 使用方法

1. 将 SSE 事件响应数据粘贴到输入框
2. 工具会自动合并所有事件并显示结果
3. 使用"复制结果"按钮复制合并后的 JSON
4. 使用"清空"按钮重置工具

## 示例输入

```
data:{"output":{"choices":[{"message":{"content":"您好","role":"assistant"},"finish_reason":"null"}]}}

data:{"output":{"choices":[{"message":{"content":"！","role":"assistant"},"finish_reason":"null"}]}}
```

## 示例输出

```json
{
  "output": {
    "choices": [
      {
        "message": {
          "content": "您好！",
          "role": "assistant"
        },
        "finish_reason": "stop"
      }
    ]
  },
  "usage": {
    "total_tokens": 916,
    "output_tokens": 46,
    "input_tokens": 870,
    "prompt_tokens_details": {
      "cached_tokens": 0
    }
  },
  "request_id": "f5724687-ce33-9b2f-8a10-cd79faafaf9c"
}
```

## 技术栈

- 纯 HTML + JavaScript 实现
- 无外部依赖
- 响应式设计

## 贡献

欢迎提交 Issue 和 Pull Request！

## 许可证

MIT License

