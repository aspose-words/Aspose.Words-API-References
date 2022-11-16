---
title: AsposeWordsPrintDocument
second_title: Aspose.Words for Java API 参考
description: 为 Java 打印框架内的打印提供默认实现。
type: docs
weight: 14
url: /zh/java/com.aspose.words/asposewordsprintdocument/
---

**遗产：**
java.lang.Object

**所有已实现的接口：**
java.awt.print.Pageable，java.awt.print.Printable
```
public class AsposeWordsPrintDocument implements Pageable, Printable
```

提供打印 a 的默认实现[Document](../../com.aspose.words/document)在 Java 打印框架中。

要了解更多信息，请访问**Printing a Document Programmatically or Using Dialogs**文档文章。

[AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument)覆盖 和 。

一个 Aspose.Words 文档可以由多个部分组成，这些部分指定具有不同尺寸、方向和纸盘的页面。[AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument)应用于正确打印每种不同的纸张尺寸、方向等。

另一方面，如果文档只包含一个部分，开发人员可以使用[AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument)以提高打印性能。
## 构造器

| 构造函数 | 描述 |
| --- | --- |
| [AsposeWordsPrintDocument(Document document)](#AsposeWordsPrintDocument-com.aspose.words.Document-) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getNumberOfPages()](#getNumberOfPages--) |  |
| [getPageFormat(int pageIndex)](#getPageFormat-int-) |  |
| [getPrintable(int pageIndex)](#getPrintable-int-) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [print(Graphics graphics, PageFormat pageFormat, int pageIndex)](#print-java.awt.Graphics-java.awt.print.PageFormat-int-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AsposeWordsPrintDocument(Document document) {#AsposeWordsPrintDocument-com.aspose.words.Document-}
```
public AsposeWordsPrintDocument(Document document)
```


初始化此类的新实例。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) | 要打印的文档。 |

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
### getNumberOfPages() {#getNumberOfPages--}
```
public int getNumberOfPages()
```




**退货：**
整数
### getPageFormat(int pageIndex) {#getPageFormat-int-}
```
public PageFormat getPageFormat(int pageIndex)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pageIndex | int |  |

**退货：**
java.awt.print.PageFormat
### getPrintable(int pageIndex) {#getPrintable-int-}
```
public Printable getPrintable(int pageIndex)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pageIndex | int |  |

**退货：**
java.awt.print.Printable
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




### print(Graphics graphics, PageFormat pageFormat, int pageIndex) {#print-java.awt.Graphics-java.awt.print.PageFormat-int-}
```
public int print(Graphics graphics, PageFormat pageFormat, int pageIndex)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| graphics | java.awt.Graphics |  |
| pageFormat | java.awt.print.PageFormat |  |
| pageIndex | int |  |

**退货：**
整数
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
