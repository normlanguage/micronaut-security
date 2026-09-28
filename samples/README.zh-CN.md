# Micronaut Security 示例

[English](README.md) | [简体中文](README.zh-CN.md)

[hello.norm](hello.norm) 是包含两个带注解路由的单文件消费者。启用安全规则后，匿名请求可访问 `/sample/public`，访问 `/sample/private` 则被拒绝。服务仅监听 `127.0.0.1:18771`。

在仓库根目录运行：

```sh
norm run samples/hello.norm
```

在另一终端比较两次响应：

```sh
curl -i 'http://127.0.0.1:18771/sample/public'
curl -i 'http://127.0.0.1:18771/sample/private'
```

预期结果：HTTP 200，正文为 `Anyone can read this`；随后 HTTP 401，响应为 `Unauthorized`。按 Ctrl+C 停止服务。本示例未配置认证提供者，因此不展示通过认证的请求。

[验收示例](../examples/sample/micronaut/security/Main.norm)另外验证身份验证响应的构造。
