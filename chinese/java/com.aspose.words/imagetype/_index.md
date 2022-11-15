---
title: ImageType
second_title: Aspose.Words for Java API 参考
description: 指定 Microsoft Word 文档中图像的类型格式。
type: docs
weight: 343
url: /zh/java/com.aspose.words/imagetype/
---

**遗产：**
java.lang.Object
```
public class ImageType
```

指定 Microsoft Word 文档中图像的类型（格式）。
## 字段

| 场地 | 描述 |
| --- | --- |
| [BMP](#BMP) | Windows 位图。 |
| [EMF](#EMF) | Windows 增强型元文件。 |
| [JPEG](#JPEG) | JPEG JFIF。 |
| [NO_IMAGE](#NO-IMAGE) | 没有图像数据。 |
| [PICT](#PICT) | Macintosh 图片。 |
| [PNG](#PNG) | 便携式网络图形。 |
| [UNKNOWN](#UNKNOWN) | 未知图像类型或无法直接存储在 Microsoft Word 文档中的图像类型。 |
| [WMF](#WMF) | Windows 图元文件。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String imageTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int imageType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int imageType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### BMP {#BMP}
```
public static int BMP
```


Windows 位图。

### EMF {#EMF}
```
public static int EMF
```


Windows 增强型元文件。

### JPEG {#JPEG}
```
public static int JPEG
```


JPEG JFIF。

### NO_IMAGE {#NO-IMAGE}
```
public static int NO_IMAGE
```


没有图像数据。

### PICT {#PICT}
```
public static int PICT
```


Macintosh 图片。现有图像将保留在文档中，但不支持将新的 PICT 图像插入到文档中。

### PNG {#PNG}
```
public static int PNG
```


便携式网络图形。

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


未知图像类型或无法直接存储在 Microsoft Word 文档中的图像类型。

### WMF {#WMF}
```
public static int WMF
```


Windows 图元文件。

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
### fromName(String imageTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String imageTypeName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imageTypeName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int imageType) {#getName-int-}
```
public static String getName(int imageType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imageType | int |  |

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
### toString(int imageType) {#toString-int-}
```
public static String toString(int imageType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imageType | int |  |

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
