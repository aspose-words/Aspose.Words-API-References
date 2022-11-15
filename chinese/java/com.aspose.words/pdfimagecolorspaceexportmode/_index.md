---
title: PdfImageColorSpaceExportMode
second_title: Aspose.Words for Java API 参考
description: 指定如何为 PDF 文档中的图像选择色彩空间。
type: docs
weight: 456
url: /zh/java/com.aspose.words/pdfimagecolorspaceexportmode/
---

**遗产:**
java.lang.Object
```
public class PdfImageColorSpaceExportMode
```

指定如何为 PDF 文档中的图像选择色彩空间。
## 字段

| 场地 | 描述 |
| --- | --- |
| [AUTO](#AUTO) | Aspose.Words 自动为每个图像选择最合适的色彩空间。 |
| [SIMPLE_CMYK](#SIMPLE-CMYK) | Aspose.Words 使用简单的公式将 RGB 图像转换为 CMYK 颜色空间。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String pdfImageColorSpaceExportModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int pdfImageColorSpaceExportMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int pdfImageColorSpaceExportMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Aspose.Words 自动为每个图像选择最合适的色彩空间。

大多数图像保存在 RGB 颜色空间中。也可以使用索引和灰度颜色空间。从不使用 CMYK 颜色空间。

对于某些图像，不同平台上的色彩空间可能不同。

### SIMPLE_CMYK {#SIMPLE-CMYK}
```
public static int SIMPLE_CMYK
```


Aspose.Words 使用简单的公式将 RGB 图像转换为 CMYK 颜色空间。

RGB 颜色空间中的图像使用以下公式转换为 CMYK：Black = minimum(1-Red,1-Green,1-Blue)。青色 = (1-红-黑)/(1-黑)。洋红色 = (1-绿色-黑色)/(1-黑色)。黄色 = (1-蓝色-黑色)/(1-黑色)。 RGB 值已标准化 - 它们介于 0 和 1.0 之间。

### length {#length}
```
public static int length
```


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
### fromName(String pdfImageColorSpaceExportModeName) {#fromName-java.lang.String-}
```
public static int fromName(String pdfImageColorSpaceExportModeName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pdfImageColorSpaceExportModeName | java.lang.String |  |

**退货:**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getName(int pdfImageColorSpaceExportMode) {#getName-int-}
```
public static String getName(int pdfImageColorSpaceExportMode)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pdfImageColorSpaceExportMode | int |  |

**退货:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**退货:**
整数[]
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




### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### toString(int pdfImageColorSpaceExportMode) {#toString-int-}
```
public static String toString(int pdfImageColorSpaceExportMode)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pdfImageColorSpaceExportMode | int |  |

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
