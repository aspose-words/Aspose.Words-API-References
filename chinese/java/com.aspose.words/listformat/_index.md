---
title: ListFormat
second_title: Aspose.Words for Java API 参考
description: 允许控制应用于段落的列表格式。
type: docs
weight: 370
url: /zh/java/com.aspose.words/listformat/
---

**遗产：**
java.lang.Object
```
public class ListFormat
```

允许控制应用于段落的列表格式。

要了解更多信息，请访问**Working with Lists**文档文章。

Microsoft Word 文档中的段落可以添加项目符号或编号。当一个段落带有项目符号或编号时，就表示该段落应用了列表格式。

您不创建对象[ListFormat](../../com.aspose.words/listformat)直接上课。您访问[ListFormat](../../com.aspose.words/listformat)作为另一个对象的属性，该对象可以具有与之关联的列表格式。目前可以具有列表格式的对象是：[Paragraph](../../com.aspose.words/paragraph), [Style](../../com.aspose.words/style)和[DocumentBuilder](../../com.aspose.words/documentbuilder).

[ListFormat](../../com.aspose.words/listformat)的[Paragraph](../../com.aspose.words/paragraph)指定应用于该特定段落的列表格式和列表级别。

[ListFormat](../../com.aspose.words/listformat)的[Style](../../com.aspose.words/style) （仅适用于段落样式）允许指定将何种列表格式和列表级别应用于该特定样式的所有段落。

[ListFormat](../../com.aspose.words/listformat)的[DocumentBuilder](../../com.aspose.words/documentbuilder)提供对当前光标位置的列表格式的访问[DocumentBuilder](../../com.aspose.words/documentbuilder).

列表格式本身存储在[List](../../com.aspose.words/list)与段落分开存储的对象。列表对象存储在一个[ListCollection](../../com.aspose.words/listcollection)收藏。有一个[ListCollection](../../com.aspose.words/listcollection)收集每[Document](../../com.aspose.words/document).

这些段落实际上不属于列表。这些段落只是通过[getList()](../../com.aspose.words/listformat\#getList--) / [setList(com.aspose.words.List)](../../com.aspose.words/listformat\#setList-com.aspose.words.List-)通过列表中的属性和特定级别[getListLevelNumber()](../../com.aspose.words/listformat\#getListLevelNumber--) / [setListLevelNumber(int)](../../com.aspose.words/listformat\#setListLevelNumber-int-)财产。通过设置这两个属性，您可以控制将哪些项目符号和编号应用于段落。
## 方法

| 方法 | 描述 |
| --- | --- |
| [applyBulletDefault()](#applyBulletDefault--) | 启动一个新的默认项目符号列表并将其应用于段落。 |
| [applyNumberDefault()](#applyNumberDefault--) | 启动一个新的默认编号列表并将其应用于段落。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getList()](#getList--) | 获取此段落所属的列表。 |
| [getListLevel()](#getListLevel--) | 返回列表级格式加上应用于当前段落的任何格式覆盖。 |
| [getListLevelNumber()](#getListLevelNumber--) | 获取段落的列表级别编号（0 到 8）。 |
| [hashCode()](#hashCode--) |  |
| [isListItem()](#isListItem--) | 当段落应用了项目符号或编号格式时为真。 |
| [listIndent()](#listIndent--) | 将当前段落的列表级别增加一级。 |
| [listOutdent()](#listOutdent--) | 将当前段落的列表级别降低一级。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeNumbers()](#removeNumbers--) | 从当前段落中删除编号或项目符号并将列表级别设置为零。 |
| [setList(List value)](#setList-com.aspose.words.List-) | 设置此段落所属的列表。 |
| [setListLevelNumber(int value)](#setListLevelNumber-int-) | 设置段落的列表级别编号（0 到 8）。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### applyBulletDefault() {#applyBulletDefault--}
```
public void applyBulletDefault()
```


启动一个新的默认项目符号列表并将其应用于段落。

这是一种使用默认项目符号模板创建新列表的快捷方法，将其应用于段落并选择第一个列表级别。

### applyNumberDefault() {#applyNumberDefault--}
```
public void applyNumberDefault()
```


启动一个新的默认编号列表并将其应用于段落。

这是一种使用默认编号模板创建新列表的快捷方法，将其应用于段落并选择第一个列表级别。

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
### getList() {#getList--}
```
public List getList()
```


获取此段落所属的列表。

分配给此属性的列表必须属于当前文档。

分配给此属性的列表不能是列表样式定义。

将此属性设置为 null 会从段落中删除项目符号和编号，并将列表级别编号设置为零。将此属性设置为 null 等效于调用[removeNumbers()](../../com.aspose.words/listformat\#removeNumbers--).

**退货：**
[List](../../com.aspose.words/list) 本段所属的列表。
### getListLevel() {#getListLevel--}
```
public ListLevel getListLevel()
```


返回列表级格式加上应用于当前段落的任何格式覆盖。

**退货：**
[ListLevel](../../com.aspose.words/listlevel) - 列表级格式以及应用于当前段落的任何格式覆盖。
### getListLevelNumber() {#getListLevelNumber--}
```
public int getListLevelNumber()
```


获取段落的列表级别编号（0 到 8）。

在 Word 文档中，列表可能由 1 或 9 个级别组成，编号为 0 到 8。

只有当[getList()](../../com.aspose.words/listformat\#getList--) / [setList(com.aspose.words.List)](../../com.aspose.words/listformat\#setList-com.aspose.words.List-)属性设置为引用有效列表。

**退货：**
int - 段落的列表级别编号（0 到 8）。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### isListItem() {#isListItem--}
```
public boolean isListItem()
```


当段落应用了项目符号或编号格式时为真。

**退货：**
boolean - 相应的布尔值。
### listIndent() {#listIndent--}
```
public void listIndent()
```


将当前段落的列表级别增加一级。

此方法更改列表级别并应用新级别的格式属性。

在 Word 文档中，列表最多可以包含九个级别。每个级别的列表格式指定使用的项目符号或编号、左缩进、项目符号和文本之间的空格等。

### listOutdent() {#listOutdent--}
```
public void listOutdent()
```


将当前段落的列表级别降低一级。

此方法更改列表级别并应用新级别的格式属性。

在 Word 文档中，列表最多可以包含九个级别。每个级别的列表格式指定使用的项目符号或编号、左缩进、项目符号和文本之间的空格等。

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### removeNumbers() {#removeNumbers--}
```
public void removeNumbers()
```


从当前段落中删除编号或项目符号并将列表级别设置为零。

调用此方法等同于设置[getList()](../../com.aspose.words/listformat\#getList--) / [setList(com.aspose.words.List)](../../com.aspose.words/listformat\#setList-com.aspose.words.List-)属性为空。

### setList(List value) {#setList-com.aspose.words.List-}
```
public void setList(List value)
```


设置此段落所属的列表。

分配给此属性的列表必须属于当前文档。

分配给此属性的列表不能是列表样式定义。

将此属性设置为 null 会从段落中删除项目符号和编号，并将列表级别编号设置为零。将此属性设置为 null 等效于调用[removeNumbers()](../../com.aspose.words/listformat\#removeNumbers--).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [List](../../com.aspose.words/list) | 此段落所属的列表。 |

### setListLevelNumber(int value) {#setListLevelNumber-int-}
```
public void setListLevelNumber(int value)
```


设置段落的列表级别编号（0 到 8）。

在 Word 文档中，列表可能由 1 或 9 个级别组成，编号为 0 到 8。

只有当[getList()](../../com.aspose.words/listformat\#getList--) / [setList(com.aspose.words.List)](../../com.aspose.words/listformat\#setList-com.aspose.words.List-)属性设置为引用有效列表。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 段落的列表级别编号（0 到 8）。 |

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
