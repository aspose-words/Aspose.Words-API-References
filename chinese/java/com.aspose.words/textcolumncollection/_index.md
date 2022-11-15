---
title: TextColumnCollection
second_title: Aspose.Words for Java API 参考
description: 表示文档的一部分中所有文本列的对象集合。
type: docs
weight: 562
url: /zh/java/com.aspose.words/textcolumncollection/
---

**遗产:**
java.lang.Object
```
public class TextColumnCollection
```

的集合[TextColumn](../../com.aspose.words/textcolumn)表示文档部分中所有文本列的对象。

要了解更多信息，请访问**Working with Sections**文档文章。

利用[setCount(int)](../../com.aspose.words/textcolumncollection\#setCount-int-)设置文本列数。

要使所有列的宽度相等且间距均匀，请设置[getEvenlySpaced()](../../com.aspose.words/textcolumncollection\#getEvenlySpaced--) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection\#setEvenlySpaced-boolean-)至**true**并指定列之间的空间量[getSpacing()](../../com.aspose.words/textcolumncollection\#getSpacing--) / [setSpacing(double)](../../com.aspose.words/textcolumncollection\#setSpacing-double-)MS Word 会自动计算列宽。

如果你有**EvenlySpaced**调成**false**，您需要分别为每一列指定宽度和间距。使用索引器访问个人[TextColumn](../../com.aspose.words/textcolumn)对象。

使用自定义列宽时，请确保所有列宽和它们之间的间距之和等于页面宽度减去左右页边距。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 返回指定索引处的文本列。 |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | 获取文档部分中的列数。 |
| [getEvenlySpaced()](#getEvenlySpaced--) | **True**如果文本列的宽度相等且间距均匀。 |
| [getLineBetween()](#getLineBetween--) | 什么时候**true**, 在列之间添加一条垂直线。 |
| [getSpacing()](#getSpacing--) | 当列均匀分布时，获取或设置每列之间的空间量（以磅为单位）。 |
| [getWidth()](#getWidth--) | 当列均匀分布时，获取列的宽度。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setCount(int newCount)](#setCount-int-) | 将文本排列到指定数量的文本列中。 |
| [setEvenlySpaced(boolean value)](#setEvenlySpaced-boolean-) | **True**如果文本列的宽度相等且间距均匀。 |
| [setLineBetween(boolean value)](#setLineBetween-boolean-) | 什么时候**true**, 在列之间添加一条垂直线。 |
| [setSpacing(double value)](#setSpacing-double-) | 当列均匀分布时，获取或设置每列之间的空间量（以磅为单位）。 |
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
### get(int index) {#get-int-}
```
public TextColumn get(int index)
```


返回指定索引处的文本列。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int |  |

**退货:**
[TextColumn](../../com.aspose.words/textcolumn) - 指定索引处的文本列。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getCount() {#getCount--}
```
public int getCount()
```


获取文档部分中的列数。

**退货:**
int - 文档部分中的列数。
### getEvenlySpaced() {#getEvenlySpaced--}
```
public boolean getEvenlySpaced()
```


**True**如果文本列的宽度相等且间距均匀。

**退货:**
boolean - 对应的布尔值。
### getLineBetween() {#getLineBetween--}
```
public boolean getLineBetween()
```


什么时候**true**, 在列之间添加一条垂直线。

**退货:**
boolean - 对应的布尔值。
### getSpacing() {#getSpacing--}
```
public double getSpacing()
```


当列均匀分布时，获取或设置每列之间的空间量（以磅为单位）。仅在以下情况下生效[getEvenlySpaced()](../../com.aspose.words/textcolumncollection\#getEvenlySpaced--) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection\#setEvenlySpaced-boolean-)被设定为**true**.

**退货:**
double - 对应的双精度值。
### getWidth() {#getWidth--}
```
public double getWidth()
```


当列均匀分布时，获取列的宽度。

仅在以下情况下生效[getEvenlySpaced()](../../com.aspose.words/textcolumncollection\#getEvenlySpaced--) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection\#setEvenlySpaced-boolean-)被设定为**true**.

**退货:**
double - 对应的双精度值。
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




### setCount(int newCount) {#setCount-int-}
```
public void setCount(int newCount)
```


将文本排列到指定数量的文本列中。

什么时候[getEvenlySpaced()](../../com.aspose.words/textcolumncollection\#getEvenlySpaced--) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection\#setEvenlySpaced-boolean-)是**false**你增加了列数，新的[TextColumn](../../com.aspose.words/textcolumn)对象以零宽度和间距创建。您需要为新列设置宽度和间距。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newCount | int | 文本要排列到的列数。 |

### setEvenlySpaced(boolean value) {#setEvenlySpaced-boolean-}
```
public void setEvenlySpaced(boolean value)
```


**True**如果文本列的宽度相等且间距均匀。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setLineBetween(boolean value) {#setLineBetween-boolean-}
```
public void setLineBetween(boolean value)
```


什么时候**true**, 在列之间添加一条垂直线。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSpacing(double value) {#setSpacing-double-}
```
public void setSpacing(double value)
```


当列均匀分布时，获取或设置每列之间的空间量（以磅为单位）。仅在以下情况下生效[getEvenlySpaced()](../../com.aspose.words/textcolumncollection\#getEvenlySpaced--) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection\#setEvenlySpaced-boolean-)被设定为**true**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 对应的双精度值。 |

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
