---
title: ConditionalStyleCollection
second_title: Aspose.Words for Java API Reference
description: 表示对象的集合。
type: docs
weight: 90
url: /zh/java/com.aspose.words/conditionalstylecollection/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Iterable
```
public class ConditionalStyleCollection implements Iterable
```

代表一个集合[ConditionalStyle](../../com.aspose.words/conditionalstyle)对象。

要了解更多信息，请访问**Working with Tables**文档文章。

无法在此集合中添加或删除项目。它包含一组永久的项目：一个项目的每个值[ConditionalStyle类型](../../com.aspose.words/conditionalstyletype)枚举类型。
## 方法

| 方法 | 描述 |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | 清除表格样式的所有条件样式。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 检索一个[ConditionalStyle](../../com.aspose.words/conditionalstyle)按索引的对象。 |
| [getBottomLeftCell()](#getBottomLeftCell--) | 获取左下角的单元格样式。 |
| [getBottomRightCell()](#getBottomRightCell--) | 获取右下角的单元格样式。 |
| [getByConditionalStyle类型(int conditionalStyle类型)](#getByConditionalStyle类型-int-) |  |
| [get班级()](#get班级--) |  |
| [getCount()](#getCount--) | 获取集合中条件样式的数量。 |
| [getEvenColumnBanding()](#getEvenColumnBanding--) | 获取偶数列条带样式。 |
| [getEvenRowBanding()](#getEvenRowBanding--) | 获取偶数行条带样式。 |
| [getFirstColumn()](#getFirstColumn--) | 获取第一个列样式。 |
| [getFirstRow()](#getFirstRow--) | 获取第一行样式。 |
| [getLastColumn()](#getLastColumn--) | 获取最后一列样式。 |
| [getLastRow()](#getLastRow--) | 获取最后一行样式。 |
| [getOddColumnBanding()](#getOddColumnBanding--) | 获取奇数列带样式。 |
| [getOddRowBanding()](#getOddRowBanding--) | 获取奇数行条带样式。 |
| [getTopLeftCell()](#getTopLeftCell--) | 获取左上角的单元格样式。 |
| [getTopRightCell()](#getTopRightCell--) | 获取右上角的单元格样式。 |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | 返回一个可用于迭代集合中所有条件样式的枚举器对象。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


清除表格样式的所有条件样式。

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
public ConditionalStyle get(int index)
```


检索一个[ConditionalStyle](../../com.aspose.words/conditionalstyle)按索引的对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 要检索的条件样式的从零开始的索引。 |

**退货:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - 相应的[ConditionalStyle](../../com.aspose.words/conditionalstyle)价值。
### getBottomLeftCell() {#getBottomLeftCell--}
```
public ConditionalStyle getBottomLeftCell()
```


获取左下角的单元格样式。

**退货:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - 左下角单元格样式。
### getBottomRightCell() {#getBottomRightCell--}
```
public ConditionalStyle getBottomRightCell()
```


获取右下角的单元格样式。

**退货:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - 右下角的单元格样式。
### getByConditionalStyle类型(int conditionalStyle类型) {#getByConditionalStyle类型-int-}
```
public ConditionalStyle getByConditionalStyle类型(int conditionalStyle类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| conditionalStyle类型 | int |  |

**退货:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle)
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getCount() {#getCount--}
```
public int getCount()
```


获取集合中条件样式的数量。

**退货:**
int - 集合中条件样式的数量。
### getEvenColumnBanding() {#getEvenColumnBanding--}
```
public ConditionalStyle getEvenColumnBanding()
```


获取偶数列条带样式。

**退货:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - 偶数列带样式。
### getEvenRowBanding() {#getEvenRowBanding--}
```
public ConditionalStyle getEvenRowBanding()
```


获取偶数行条带样式。

**退货:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - 偶数行镶边样式。
### getFirstColumn() {#getFirstColumn--}
```
public ConditionalStyle getFirstColumn()
```


获取第一个列样式。

**退货:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - 第一列样式。
### getFirstRow() {#getFirstRow--}
```
public ConditionalStyle getFirstRow()
```


获取第一行样式。

**退货:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - 第一行样式。
### getLastColumn() {#getLastColumn--}
```
public ConditionalStyle getLastColumn()
```


获取最后一列样式。

**退货:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - 最后一列样式。
### getLastRow() {#getLastRow--}
```
public ConditionalStyle getLastRow()
```


获取最后一行样式。

**退货:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - 最后一行样式。
### getOddColumnBanding() {#getOddColumnBanding--}
```
public ConditionalStyle getOddColumnBanding()
```


获取奇数列带样式。

**退货:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - 奇怪的列带样式。
### getOddRowBanding() {#getOddRowBanding--}
```
public ConditionalStyle getOddRowBanding()
```


获取奇数行条带样式。

**退货:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - 奇数行带样式。
### getTopLeftCell() {#getTopLeftCell--}
```
public ConditionalStyle getTopLeftCell()
```


获取左上角的单元格样式。

**退货:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - 左上角的单元格样式。
### getTopRightCell() {#getTopRightCell--}
```
public ConditionalStyle getTopRightCell()
```


获取右上角的单元格样式。

**退货:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - 右上角的单元格样式。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### iterator() {#iterator--}
```
public Iterator iterator()
```


返回一个可用于迭代集合中所有条件样式的枚举器对象。

**退货:**
java.util.Iterator
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
