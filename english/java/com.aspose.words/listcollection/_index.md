---
title: ListCollection
second_title: Aspose.Words for Java API 参考
description: 存储和管理文档中使用的项目符号和编号列表的格式。
type: docs
weight: 369
url: /zh/java/com.aspose.words/listcollection/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Cloneable, java.lang.Iterable
```
public class ListCollection implements Cloneable, Iterable
```

存储和管理文档中使用的项目符号和编号列表的格式。

要了解更多信息，请访问**Working with Lists**文档文章。

 Microsoft Word 文档中的列表是一组列表格式属性。列表的格式存储在[ListCollection](../../com.aspose.words/listcollection)与文本段落分开收集。

您不创建此类的对象。永远只有一个[ListCollection](../../com.aspose.words/listcollection)每个文档的对象，并且可以通过[DocumentBase.getLists()](../../com.aspose.words/documentbase\#getLists--)财产。

要基于预定义的列表模板或列表样式创建新列表，请使用[add(com.aspose.words.Style)](../../com.aspose.words/listcollection\#add-com.aspose.words.Style-)方法。

要创建格式与现有列表相同的新列表，请使用[addCopy(com.aspose.words.List)](../../com.aspose.words/listcollection\#addCopy-com.aspose.words.List-)方法。

要使段落带有项目符号或编号，您需要通过分配[List](../../com.aspose.words/list)反对[ListFormat.getList()](../../com.aspose.words/listformat\#getList--) / [ListFormat.setList(com.aspose.words.List)](../../com.aspose.words/listformat\#setList-com.aspose.words.List-)的财产[ListFormat](../../com.aspose.words/listformat).

要从段落中删除列表格式，请使用[ListFormat.removeNumbers()](../../com.aspose.words/listformat\#removeNumbers--)方法。

如果您对 WordprocessingML 有所了解，那么您可能知道它为“列表”和“列表定义”定义了不同的概念。这与列表格式在低级别 Microsoft Word 文档中的存储方式完全一致。列表定义就像一个“模式”，列表就像一个列表定义的实例。

为了简化编程模型，Aspose.Words 隐藏了列表和列表定义之间的区别，就像 Microsoft Word 在其用户界面中隐藏它一样。这使您可以更专注于您希望文档的外观，而不是构建低级对象以满足 Microsoft Word 文件格式的要求。

一旦在当前版本的 Aspose.Words 中创建列表，就无法删除它们。这类似于 Microsoft Word，其中用户没有对列表定义的显式控制。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [add(Style listStyle)](#add-com.aspose.words.Style-) | 创建一个引用列表样式的新列表，并将其添加到文档中的列表集合中。 |
| [add(int listTemplate)](#add-int-) |  |
| [addCopy(List srcList)](#addCopy-com.aspose.words.List-) | 通过复制指定列表并将其添加到文档中的列表集合来创建一个新列表。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 按索引获取列表。 |
| [get班级()](#get班级--) |  |
| [getCount()](#getCount--) | 获取文档中编号和项目符号列表的计数。 |
| [getDocument()](#getDocument--) | 获取所有者文档。 |
| [getListByListId(int listId)](#getListByListId-int-) | 通过列表标识符获取列表。 |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | 获取将枚举文档中列表的枚举器对象。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(Style listStyle) {#add-com.aspose.words.Style-}
```
public List add(Style listStyle)
```


创建一个引用列表样式的新列表，并将其添加到文档中的列表集合中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| listStyle | [Style](../../com.aspose.words/style) | 列表样式。 |

**退货:**
[List](../../com.aspose.words/list) - 新创建的列表。

新创建的列表引用列表样式。如果更改列表样式的属性，它会反映在列表的属性中。反之亦然，如果更改列表的属性，它会反映在列表样式的属性中。
### add(int listTemplate) {#add-int-}
```
public List add(int listTemplate)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| listTemplate | int |  |

**退货:**
[List](../../com.aspose.words/list)
### addCopy(List srcList) {#addCopy-com.aspose.words.List-}
```
public List addCopy(List srcList)
```


通过复制指定列表并将其添加到文档中的列表集合来创建一个新列表。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcList | [List](../../com.aspose.words/list) | 要从中复制的源列表。 |

**退货:**
[List](../../com.aspose.words/list) - 新创建的列表。

源列表可以来自任何文档。如果源列表属于不同的文档，则会创建列表的副本并将其添加到当前文档。

如果源列表是对列表样式的引用或定义，则新创建的列表与原始列表样式无关。
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
public List get(int index)
```


按索引获取列表。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int |  |

**退货:**
[List](../../com.aspose.words/list) - 按索引列出。
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


获取文档中编号和项目符号列表的计数。

**退货:**
int - 文档中编号和项目符号列表的计数。
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


获取所有者文档。

**退货:**
[DocumentBase](../../com.aspose.words/documentbase) - 所有者文件。
### getListByListId(int listId) {#getListByListId-int-}
```
public List getListByListId(int listId)
```


通过列表标识符获取列表。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| listId | int | 列表标识符。 |

**退货:**
[List](../../com.aspose.words/list) - 返回列表对象。如果未找到具有指定标识符的列表，则返回 null。

您通常不需要使用此方法。大多数情况下，您只需通过设置[ListFormat.getList()](../../com.aspose.words/listformat\#getList--) / [ListFormat.setList(com.aspose.words.List)](../../com.aspose.words/listformat\#setList-com.aspose.words.List-)的财产[ListFormat](../../com.aspose.words/listformat)目的。
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


获取将枚举文档中列表的枚举器对象。

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
