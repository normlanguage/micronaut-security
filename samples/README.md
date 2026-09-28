# Micronaut Security samples

[English](README.md) | [简体中文](README.zh-CN.md)

[hello.norm](hello.norm) is a single-file consumer with two annotated routes. With security enabled, an anonymous request is allowed at `/sample/public` and rejected at `/sample/private`. The server binds only to `127.0.0.1:18771`.

From the repository root, run:

```sh
norm run samples/hello.norm
```

In another terminal, compare both responses:

```sh
curl -i 'http://127.0.0.1:18771/sample/public'
curl -i 'http://127.0.0.1:18771/sample/private'
```

Expected results: HTTP 200 with `Anyone can read this`, then HTTP 401 with an `Unauthorized` response. Stop the server with Ctrl+C. This sample does not configure an authentication provider, so it does not demonstrate a successful authenticated request.

The [acceptance example](../examples/sample/micronaut/security/Main.norm) checks authentication response construction separately.
