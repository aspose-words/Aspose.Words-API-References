---
title: PdfDigitalSignatureTimestampSettings
second_title: Aspose.Words for Java API 参考
description: 包含数字签名时间戳的设置。
type: docs
weight: 453
url: /zh/java/com.aspose.words/pdfdigitalsignaturetimestampsettings/
---

**遗产:**
java.lang.Object
```
public class PdfDigitalSignatureTimestampSettings
```

包含数字签名时间戳的设置。

要了解更多信息，请访问**Work with Digital Signatures**文档文章。
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [PdfDigitalSignatureTimestampSettings()](#PdfDigitalSignatureTimestampSettings--) | 初始化此类的实例。 |
| [PdfDigitalSignatureTimestampSettings(String serverUrl, String userName, String password)](#PdfDigitalSignatureTimestampSettings-java.lang.String-java.lang.String-java.lang.String-) | 初始化此类的实例。 |
| [PdfDigitalSignatureTimestampSettings(String serverUrl, String userName, String password, long timeout)](#PdfDigitalSignatureTimestampSettings-java.lang.String-java.lang.String-java.lang.String-long-) | 初始化此类的实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getPassword()](#getPassword--) | 时间戳服务器密码。 |
| [getServerUrl()](#getServerUrl--) | 时间戳服务器 URL。 |
| [getTimeout()](#getTimeout--) | 访问时间戳服务器的超时值（以毫秒为单位）。 |
| [getUserName()](#getUserName--) | 时间戳服务器用户名。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setPassword(String value)](#setPassword-java.lang.String-) | 时间戳服务器密码。 |
| [setServerUrl(String value)](#setServerUrl-java.lang.String-) | 时间戳服务器 URL。 |
| [setTimeout(long value)](#setTimeout-long-) | 访问时间戳服务器的超时值（以毫秒为单位）。 |
| [setUserName(String value)](#setUserName-java.lang.String-) | 时间戳服务器用户名。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### PdfDigitalSignatureTimestampSettings() {#PdfDigitalSignatureTimestampSettings--}
```
public PdfDigitalSignatureTimestampSettings()
```


初始化此类的实例。

### PdfDigitalSignatureTimestampSettings(String serverUrl, String userName, String password) {#PdfDigitalSignatureTimestampSettings-java.lang.String-java.lang.String-java.lang.String-}
```
public PdfDigitalSignatureTimestampSettings(String serverUrl, String userName, String password)
```


初始化此类的实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| serverUrl | java.lang.String | 时间戳服务器 URL。 |
| userName | java.lang.String | 时间戳服务器用户名。 |
| password | java.lang.String | 时间戳服务器密码。 |

### PdfDigitalSignatureTimestampSettings(String serverUrl, String userName, String password, long timeout) {#PdfDigitalSignatureTimestampSettings-java.lang.String-java.lang.String-java.lang.String-long-}
```
public PdfDigitalSignatureTimestampSettings(String serverUrl, String userName, String password, long timeout)
```


初始化此类的实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| serverUrl | java.lang.String | 时间戳服务器 URL。 |
| userName | java.lang.String | 时间戳服务器用户名。 |
| password | java.lang.String | 时间戳服务器密码。 |
| timeout | long | 访问时间戳服务器的超时值（以毫秒为单位）。 |

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getPassword() {#getPassword--}
```
public String getPassword()
```


时间戳服务器密码。默认值为空。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getServerUrl() {#getServerUrl--}
```
public String getServerUrl()
```


时间戳服务器 URL。默认值为空。如果为空，则数字签名将不带有时间戳。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getTimeout() {#getTimeout--}
```
public long getTimeout()
```


访问时间戳服务器的超时值（以毫秒为单位）。默认值为 100 秒。

**退货:**
long - 相应的 long 值。
### getUserName() {#getUserName--}
```
public String getUserName()
```


时间戳服务器用户名。默认值为空。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setPassword(String value) {#setPassword-java.lang.String-}
```
public void setPassword(String value)
```


时间戳服务器密码。默认值为空。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setServerUrl(String value) {#setServerUrl-java.lang.String-}
```
public void setServerUrl(String value)
```


时间戳服务器 URL。默认值为空。如果为空，则数字签名将不带有时间戳。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setTimeout(long value) {#setTimeout-long-}
```
public void setTimeout(long value)
```


访问时间戳服务器的超时值（以毫秒为单位）。默认值为 100 秒。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | long | 对应的长值。 |

### setUserName(String value) {#setUserName-java.lang.String-}
```
public void setUserName(String value)
```


时间戳服务器用户名。默认值为空。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
