---
title: SignOptions
second_title: Aspose.Words for Java API 参考
description: 允许指定文档签名的选项。
type: docs
weight: 523
url: /zh/java/com.aspose.words/signoptions/
---

**遗产：**
java.lang.Object
```
public class SignOptions
```

允许指定文档签名的选项。

要了解更多信息，请访问**Work with Digital Signatures**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getComments()](#getComments--) | 指定对数字签名的注释。 |
| [getDecryptionPassword()](#getDecryptionPassword--) | 解密源文档的密码。 |
| [getProviderId()](#getProviderId--) | 指定签名提供者的类 ID。 |
| [getSignTime()](#getSignTime--) | 签署日期。 |
| [getSignatureLineId()](#getSignatureLineId--) | 签名行标识符。 |
| [getSignatureLineImage()](#getSignatureLineImage--) | 将在关联中显示的图像[SignatureLine](../../com.aspose.words/signatureline). |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setComments(String value)](#setComments-java.lang.String-) | 指定对数字签名的注释。 |
| [setDecryptionPassword(String value)](#setDecryptionPassword-java.lang.String-) | 解密源文档的密码。 |
| [setProviderId(UUID value)](#setProviderId-java.util.UUID-) | 指定签名提供者的类 ID。 |
| [setSignTime(Date value)](#setSignTime-java.util.Date-) | 签署日期。 |
| [setSignatureLineId(UUID value)](#setSignatureLineId-java.util.UUID-) | 签名行标识符。 |
| [setSignatureLineImage(byte[] value)](#setSignatureLineImage-byte---) | 将在关联中显示的图像[SignatureLine](../../com.aspose.words/signatureline). |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getComments() {#getComments--}
```
public String getComments()
```


指定对数字签名的注释。默认值为**empty string**.

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getDecryptionPassword() {#getDecryptionPassword--}
```
public String getDecryptionPassword()
```


解密源文档的密码。默认值为**empty string**.如果 OOXML 文档是加密的，您应该在签名之前提供解密密码来解密源文档。二进制 DOC 格式的文档不需要这样做。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getProviderId() {#getProviderId--}
```
public UUID getProviderId()
```


指定签名提供者的类 ID。默认值为**Empty (all zeroes) Guid**.

加密服务提供者 (CSP) 是一个独立的软件模块，它实际上执行用于身份验证、编码和加密的加密算法。 MS Office 保留的价值\{00000000-0000-0000-0000-000000000000\为其默认签名提供者。

额外安装的提供程序的 GUID 应从提供程序随附的文档中获取。

此外，所有已安装的加密提供程序都在 Windows 注册表中枚举。可以在以下路径中找到：HKLM\\软件\\微软\\密码学\\默认值\\提供者。有一个密钥名称“CP Service UUID”，它对应于签名提供者的 GUID。

**退货：**
java.util.UUID - 相应的 java.util.UUID 值。
### getSignTime() {#getSignTime--}
```
public Date getSignTime()
```


签署日期。默认值为**current time**.

**退货：**
java.util.Date - 相应的 java.util.Date 值。
### getSignatureLineId() {#getSignatureLineId--}
```
public UUID getSignatureLineId()
```


签名行标识符。默认值为**Empty (all zeroes) Guid**.设置时，它关联[SignatureLine](../../com.aspose.words/signatureline)与相应的[DigitalSignature](../../com.aspose.words/digitalsignature).

**退货：**
java.util.UUID - 相应的 java.util.UUID 值。
### getSignatureLineImage() {#getSignatureLineImage--}
```
public byte[] getSignatureLineImage()
```


将在关联中显示的图像[SignatureLine](../../com.aspose.words/signatureline).默认值为 null 。

**退货：**
字节[- 对应的字节[] 价值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setComments(String value) {#setComments-java.lang.String-}
```
public void setComments(String value)
```


指定对数字签名的注释。默认值为**empty string**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setDecryptionPassword(String value) {#setDecryptionPassword-java.lang.String-}
```
public void setDecryptionPassword(String value)
```


解密源文档的密码。默认值为**empty string**.如果 OOXML 文档是加密的，您应该在签名之前提供解密密码来解密源文档。二进制 DOC 格式的文档不需要这样做。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setProviderId(UUID value) {#setProviderId-java.util.UUID-}
```
public void setProviderId(UUID value)
```


指定签名提供者的类 ID。默认值为**Empty (all zeroes) Guid**.

加密服务提供者 (CSP) 是一个独立的软件模块，它实际上执行用于身份验证、编码和加密的加密算法。 MS Office 保留的价值\{00000000-0000-0000-0000-000000000000\为其默认签名提供者。

额外安装的提供程序的 GUID 应从提供程序随附的文档中获取。

此外，所有已安装的加密提供程序都在 Windows 注册表中枚举。可以在以下路径中找到：HKLM\\软件\\微软\\密码学\\默认值\\提供者。有一个密钥名称“CP Service UUID”，它对应于签名提供者的 GUID。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.util.UUID | 对应的 java.util.UUID 值。 |

### setSignTime(Date value) {#setSignTime-java.util.Date-}
```
public void setSignTime(Date value)
```


签署日期。默认值为**current time**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.util.Date | 对应的 java.util.Date 值。 |

### setSignatureLineId(UUID value) {#setSignatureLineId-java.util.UUID-}
```
public void setSignatureLineId(UUID value)
```


签名行标识符。默认值为**Empty (all zeroes) Guid**.设置时，它关联[SignatureLine](../../com.aspose.words/signatureline)与相应的[DigitalSignature](../../com.aspose.words/digitalsignature).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.util.UUID | 对应的 java.util.UUID 值。 |

### setSignatureLineImage(byte[] value) {#setSignatureLineImage-byte---}
```
public void setSignatureLineImage(byte[] value)
```


将在关联中显示的图像[SignatureLine](../../com.aspose.words/signatureline).默认值为 null 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | byte[] | 对应的字节[] 价值。 |

### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
