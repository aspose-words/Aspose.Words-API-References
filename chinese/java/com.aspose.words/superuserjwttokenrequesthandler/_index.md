---
title: "SuperUserJwtTokenRequestHandler"
linktitle: "SuperUserJwtTokenRequestHandler"
second_title: "Aspose.Words for Java"
description: "JWT 令牌请求处理程序，具备缓存、本地验证和 Java 中的断路器。"
type: docs
weight: 648
url: /zh/java/com.aspose.words/superuserjwttokenrequesthandler/
---

**Inheritance:**
java.lang.Object
```
public class SuperUserJwtTokenRequestHandler
```

JWT 令牌请求处理程序，具备缓存、本地验证和断路器。令牌缓存最长 7 天，并在过期前 6 小时刷新。
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [SuperUserJwtTokenRequestHandler()](#SuperUserJwtTokenRequestHandler) | 公共构造函数。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [beforeSend(HttpURLConnection request, OutputStream streamToSend)](#beforeSend-java.net.HttpURLConnection-java.io.OutputStream) | 在发送请求之前添加授权头。 |
| [getCachedToken()](#getCachedToken) | 获取当前缓存的令牌（用于测试）。 |
| [getTokenExpiration()](#getTokenExpiration) | 获取令牌的过期日期（用于测试）。 |
| [getTokenExpirationMillis()](#getTokenExpirationMillis) | 获取令牌的过期时间（用于测试）。 |
| [processResponse(HttpURLConnection response, String resultString, String errorString)](#processResponse-java.net.HttpURLConnection-java.lang.String-java.lang.String) | 处理响应，遇到 401 未授权时通过刷新令牌处理。 |
| [processUrl(String url)](#processUrl-java.lang.String) | 处理 URL（确保令牌可用）。 |
| [resetForTesting()](#resetForTesting) | 重置所有缓存的令牌状态（用于测试）。 |
### SuperUserJwtTokenRequestHandler() {#SuperUserJwtTokenRequestHandler}
```
public SuperUserJwtTokenRequestHandler()
```


公共构造函数。

### beforeSend(HttpURLConnection request, OutputStream streamToSend) {#beforeSend-java.net.HttpURLConnection-java.io.OutputStream}
```
public void beforeSend(HttpURLConnection request, OutputStream streamToSend)
```


在发送请求之前添加授权头。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 请求 | java.net.HttpURLConnection | HTTP 连接 |
| streamToSend | java.io.OutputStream | 输出流（未使用） |

### getCachedToken() {#getCachedToken}
```
public static String getCachedToken()
```


获取当前缓存的令牌（用于测试）。

**Returns:**
java.lang.String - 缓存的 JWT 令牌或 null
### getTokenExpiration() {#getTokenExpiration}
```
public static Date getTokenExpiration()
```


获取令牌的过期日期（用于测试）。

**Returns:**
java.util.Date - 过期日期或如果没有令牌则为 null
### getTokenExpirationMillis() {#getTokenExpirationMillis}
```
public static long getTokenExpirationMillis()
```


获取令牌的过期时间（用于测试）。

**Returns:**
long - 自纪元以来的毫秒数表示的过期时间
### processResponse(HttpURLConnection response, String resultString, String errorString) {#processResponse-java.net.HttpURLConnection-java.lang.String-java.lang.String}
```
public void processResponse(HttpURLConnection response, String resultString, String errorString)
```


处理响应，遇到 401 未授权时通过刷新令牌处理。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| response | java.net.HttpURLConnection | HTTP 响应 |
| resultString | java.lang.String | 响应正文 |
| errorString | java.lang.String | 错误信息（如果有） |

### processUrl(String url) {#processUrl-java.lang.String}
```
public String processUrl(String url)
```


处理 URL（确保令牌可用）。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| url | java.lang.String | 要处理的 URL |

**Returns:**
java.lang.String - 未更改的 URL
### resetForTesting() {#resetForTesting}
```
public static void resetForTesting()
```


重置所有缓存的令牌状态（用于测试）。

