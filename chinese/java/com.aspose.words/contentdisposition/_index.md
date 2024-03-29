---
title: ContentDisposition
second_title: Aspose.Words for Java API 参考
description: 枚举在客户端浏览器中呈现文档的不同方式。
type: docs
weight: 92
url: /zh/java/com.aspose.words/contentdisposition/
---

**遗产：**
java.lang.Object
```
public class ContentDisposition
```

枚举在客户端浏览器中呈现文档的不同方式。

请注意，客户端浏览器上的实际行为可能会受到浏览器安全配置的影响。
## 字段

| 场地 | 描述 |
| --- | --- |
| [ATTACHMENT](#ATTACHMENT) | 将文档发送到浏览器并显示将文档保存到磁盘或在与文档扩展名关联的应用程序中打开的选项。 |
| [INLINE](#INLINE) | 将文档发送到浏览器并显示将文档保存到磁盘或在浏览器中打开的选项。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String contentDispositionName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int contentDisposition)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int contentDisposition)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ATTACHMENT {#ATTACHMENT}
```
public static int ATTACHMENT
```


将文档发送到浏览器并显示将文档保存到磁盘或在与文档扩展名关联的应用程序中打开的选项。

### INLINE {#INLINE}
```
public static int INLINE
```


将文档发送到浏览器并显示将文档保存到磁盘或在浏览器中打开的选项。

### length {#length}
```
public static int length
```


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
### fromName(String contentDispositionName) {#fromName-java.lang.String-}
```
public static int fromName(String contentDispositionName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| contentDispositionName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int contentDisposition) {#getName-int-}
```
public static String getName(int contentDisposition)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| contentDisposition | int |  |

**退货：**
java.lang.字符串
### getValues() {#getValues--}
```
public static int[] getValues()
```




**退货：**
整数[]
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




### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### toString(int contentDisposition) {#toString-int-}
```
public static String toString(int contentDisposition)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| contentDisposition | int |  |

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
