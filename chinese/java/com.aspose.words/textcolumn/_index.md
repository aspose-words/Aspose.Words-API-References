---
title: TextColumn
second_title: Aspose.Words for Java API Reference
description: 表示单个文本列。
type: docs
weight: 561
url: /zh/java/com.aspose.words/textcolumn/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Cloneable
```
public class TextColumn implements Cloneable
```

表示单个文本列。**TextColumn**是成员[TextColumnCollection](../../com.aspose.words/textcolumncollection)收藏。这**TextColumns**集合包括文档部分中的所有列。

要了解更多信息，请访问**Working with Sections**文档文章。

**TextColumn**对象仅用于指定具有自定义宽度和间距的列。如果您希望文档中的列等宽，请设置 TextColumns。[TextColumnCollection.getEvenlySpaced()](../../com.aspose.words/textcolumncollection\#getEvenlySpaced--) / [TextColumnCollection.setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection\#setEvenlySpaced-boolean-)至**true**.

当一个新的**TextColumn**创建它的宽度和间距设置为零。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getSpaceAfter()](#getSpaceAfter--) | 获取此列与下一列之间的空间（以磅为单位）。 |
| [getWidth()](#getWidth--) | 获取文本列的宽度（以磅为单位）。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setSpaceAfter(double value)](#setSpaceAfter-double-) | 设置此列和下一列之间的间距（以磅为单位）。 |
| [setWidth(double value)](#setWidth-double-) | 以磅为单位设置文本列的宽度。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getSpaceAfter() {#getSpaceAfter--}
```
public double getSpaceAfter()
```


获取此列与下一列之间的空间（以磅为单位）。最后一列不需要。

**退货:**
double - 此列与下一列之间的间距（以磅为单位）。
### getWidth() {#getWidth--}
```
public double getWidth()
```


获取文本列的宽度（以磅为单位）。

**退货:**
double - 文本列的宽度（以磅为单位）。
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




### setSpaceAfter(double value) {#setSpaceAfter-double-}
```
public void setSpaceAfter(double value)
```


设置此列和下一列之间的间距（以磅为单位）。最后一列不需要。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 此列与下一列之间的空间（以磅为单位）。 |

### setWidth(double value) {#setWidth-double-}
```
public void setWidth(double value)
```


以磅为单位设置文本列的宽度。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 文本列的宽度（以磅为单位）。 |

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
