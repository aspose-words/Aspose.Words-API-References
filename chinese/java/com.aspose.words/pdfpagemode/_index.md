---
title: PdfPageMode
second_title: Aspose.Words for Java API 参考
description: 指定在 PDF 阅读器中打开 PDF 文档时应如何显示。
type: docs
weight: 459
url: /zh/java/com.aspose.words/pdfpagemode/
---

**遗产：**
java.lang.Object
```
public class PdfPageMode
```

指定在 PDF 阅读器中打开 PDF 文档时应如何显示。
## 字段

| 场地 | 描述 |
| --- | --- |
| [FULL_SCREEN](#FULL-SCREEN) | 全屏模式，没有菜单栏、窗口控件或任何其他可见窗口。 |
| [USE_ATTACHMENTS](#USE-ATTACHMENTS) | 附件面板可见。 |
| [USE_NONE](#USE-NONE) | 文档大纲和缩略图图像都不可见。 |
| [USE_OC](#USE-OC) | 可选内容组面板可见。 |
| [USE_OUTLINES](#USE-OUTLINES) | 文档大纲可见。 |
| [USE_THUMBS](#USE-THUMBS) | 缩略图是可见的。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String pdfPageModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int pdfPageMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int pdfPageMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### FULL_SCREEN {#FULL-SCREEN}
```
public static int FULL_SCREEN
```


全屏模式，没有菜单栏、窗口控件或任何其他可见窗口。

### USE_ATTACHMENTS {#USE-ATTACHMENTS}
```
public static int USE_ATTACHMENTS
```


附件面板可见。以下 PDF 版本不支持：[PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance\#PDF-A-1-B).

### USE_NONE {#USE-NONE}
```
public static int USE_NONE
```


文档大纲和缩略图图像都不可见。

### USE_OC {#USE-OC}
```
public static int USE_OC
```


可选内容组面板可见。以下 PDF 版本不支持：[PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance\#PDF-A-1-B).

### USE_OUTLINES {#USE-OUTLINES}
```
public static int USE_OUTLINES
```


文档大纲可见。请注意，如果 PDF 文档中没有大纲，那么无论如何大纲导航窗格都将不可见。

### USE_THUMBS {#USE-THUMBS}
```
public static int USE_THUMBS
```


缩略图是可见的。

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
### fromName(String pdfPageModeName) {#fromName-java.lang.String-}
```
public static int fromName(String pdfPageModeName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pdfPageModeName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int pdfPageMode) {#getName-int-}
```
public static String getName(int pdfPageMode)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pdfPageMode | int |  |

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
### toString(int pdfPageMode) {#toString-int-}
```
public static String toString(int pdfPageMode)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pdfPageMode | int |  |

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
