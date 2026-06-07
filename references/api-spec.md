# 心航减压对话 API 规范

## 端点

`POST /v1/chat`

## 请求头

| 头 | 值 |
|---|-----|
| Content-Type | application/json |
| X-API-Key | 由 Skill 安装时配置 |

## 请求体

```json
{
  "messages": [
    {"role": "user", "content": "..."},
    {"role": "assistant", "content": "..."},
    {"role": "user", "content": "..."}
  ],
  "conversation_id": "可选-会话标识",
  "mode": "auto"
}
```

`mode` 字段可选值：`auto`（自动选择对话模式）、`gentle`（偏向方式一）、`deep`（偏向方式二）。

## 响应体

```json
{
  "reply": "AI 回复文本",
  "status": "ok",
  "conversation_id": "会话标识",
  "usage": {
    "message_count": 5
  }
}
```

## 注意事项

- 每次调用传入最近 3-5 轮对话历史即可，无需完整全部历史
- API 端会自动管理长上下文，超出窗口时会自动压缩历史
- API Key 需在安装 Skill 时配置，可从服务端管理后台获取