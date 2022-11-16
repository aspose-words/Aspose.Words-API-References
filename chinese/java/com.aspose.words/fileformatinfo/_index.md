---
title: FileFormatInfo
second_title: Aspose.Words for Java API 参考
description: 包含文档格式检测方法返回的数据。
type: docs
weight: 265
url: /zh/java/com.aspose.words/fileformatinfo/
---

**遗产：**
java.lang.Object
```
public class FileFormatInfo
```

包含由返回的数据[FileFormatUtil](../../com.aspose.words/fileformatutil)文档格式检测方法。

要了解更多信息，请访问**Detect File Format and Check Format Compatibility**文档文章。

您不直接创建此类的实例。此类的对象由**M:Aspose.Words.FileFormatUtil.DetectFileFormat(System.IO.Stream)**方法。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getEncoding()](#getEncoding--) | 如果适用于当前文档格式，则获取检测到的编码。 |
| [getLoadFormat()](#getLoadFormat--) | 获取检测到的文档格式。 |
| [hasDigitalSignature()](#hasDigitalSignature--) | 如果此文档包含数字签名，则返回 true。 |
| [hashCode()](#hashCode--) |  |
| [isEncrypted()](#isEncrypted--) | 如果文档已加密并需要密码才能打开，则返回 true。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
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
### getEncoding() {#getEncoding--}
```
public Charset getEncoding()
```


如果适用于当前文档格式，则获取检测到的编码。目前仅检测 HTML 文档的编码。

**退货：**
java.nio.charset.Charset - 如果适用于当前文档格式，则检测到的编码。
### getLoadFormat() {#getLoadFormat--}
```
public int getLoadFormat()
```


获取检测到的文档格式。

当 OOXML 文档被加密时，如果不先解密它是不可能确定它是 Excel、Word 还是 PowerPoint 文档，因此对于加密的 OOXML 文档，此属性将始终返回[LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX).

**退货：**
int - 检测到的文档格式。返回值是其中之一[LoadFormat](../../com.aspose.words/loadformat)常数。
### hasDigitalSignature() {#hasDigitalSignature--}
```
public boolean hasDigitalSignature()
```


如果此文档包含数字签名，则返回 true。此属性仅通知文档上存在数字签名，但不指定签名是否有效。

此属性的存在是为了帮助您将经过数字签名的文档与未经过数字签名的文档分类。如果您使用 Aspose.Words 修改并保存经过数字签名的文档，则数字签名将丢失。这是设计使然，因为存在数字签名以保护文档的真实性。使用此属性，您可以在以与普通文档相同的方式处理它们之前检测数字签名的文档，并采取一些措施来避免丢失数字签名，例如通知用户。

**退货：**
boolean - 如果此文档包含数字签名，则为真。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### isEncrypted() {#isEncrypted--}
```
public boolean isEncrypted()
```


如果文档已加密并需要密码才能打开，则返回 true。

此属性的存在是为了帮助您对已加密的文档和未加密的文档进行排序。如果您尝试使用 Aspose.Words 加载加密文档而不提供密码，则会引发异常。您可以使用此属性来检测文档是否需要密码并在加载文档之前执行一些操作，例如提示用户输入密码。

**退货：**
boolean - 如果文档已加密且需要密码才能打开，则为 True。
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




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
