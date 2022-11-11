---
title: LayoutCollector
second_title: Aspose.Words for Java API 参考
description: 此类允许计算文档节点的页码。
type: docs
weight: 358
url: /zh/java/com.aspose.words/layoutcollector/
---

**遗产:**
java.lang.Object
```
public class LayoutCollector
```

此类允许计算文档节点的页码。

要了解更多信息，请访问**Converting to Fixed-page Format**文档文章。

当你创建一个[LayoutCollector](../../com.aspose.words/layoutcollector)并指定一个[Document](../../com.aspose.words/document)要附加到的文档对象，当文档被格式化为页面时，收集器将记录文档节点到布局对象的映射。

您将能够通过使用[getStartPageIndex(com.aspose.words.Node)](../../com.aspose.words/layoutcollector\#getStartPageIndex-com.aspose.words.Node-), [getEndPageIndex(com.aspose.words.Node)](../../com.aspose.words/layoutcollector\#getEndPageIndex-com.aspose.words.Node-)和[getNumPagesSpanned(com.aspose.words.Node)](../../com.aspose.words/layoutcollector\#getNumPagesSpanned-com.aspose.words.Node-)方法。如果需要，这些方法会自动构建文档的页面布局模型并更新字段。

当您不再需要收集布局信息时，最好将[getDocument()](../../com.aspose.words/layoutcollector\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/layoutcollector\#setDocument-com.aspose.words.Document-)属性为 null 以避免不必要地收集更多布局映射。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [LayoutCollector(Document doc)](#LayoutCollector-com.aspose.words.Document-) | 初始化此类的一个实例。 |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [clear()](#clear--) | 清除所有收集的布局数据。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getDocument()](#getDocument--) | 获取此收集器实例附加到的文档。 |
| [getEndPageIndex(Node node)](#getEndPageIndex-com.aspose.words.Node-) | 获取节点结束的页面的从 1 开始的索引。 |
| [getEntity(Node node)](#getEntity-com.aspose.words.Node-) | 返回一个不透明的位置[LayoutEnumerator](../../com.aspose.words/layoutenumerator)它对应于指定的节点。 |
| [getNumPagesSpanned(Node node)](#getNumPagesSpanned-com.aspose.words.Node-) | 获取指定节点跨越的页数。 |
| [getStartPageIndex(Node node)](#getStartPageIndex-com.aspose.words.Node-) | 获取节点开始的页面的从 1 开始的索引。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setDocument(Document value)](#setDocument-com.aspose.words.Document-) | 设置此收集器实例附加到的文档。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### LayoutCollector(Document doc) {#LayoutCollector-com.aspose.words.Document-}
```
public LayoutCollector(Document doc)
```


初始化此类的一个实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document) | 此收集器实例将附加到的文档。 |

### clear() {#clear--}
```
public void clear()
```


清除所有收集的布局数据。在手动更新文档或重新构建布局后调用此方法。

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
### getDocument() {#getDocument--}
```
public Document getDocument()
```


获取此收集器实例附加到的文档。如果您需要访问文档节点的页面索引，则需要在构建文档的页面布局之前将此属性设置为指向文档实例。最好在之后将此属性设置为 null，否则收集器会继续从文档页面布局的后续重建中积累信息。

**退货:**
[Document](../../com.aspose.words/document) - 此收集器实例附加到的文档。
### getEndPageIndex(Node node) {#getEndPageIndex-com.aspose.words.Node-}
```
public int getEndPageIndex(Node node)
```


获取节点结束的页面的从 1 开始的索引。如果节点无法映射到页面，则返回 0。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) |  |

**退货:**
整数
### getEntity(Node node) {#getEntity-com.aspose.words.Node-}
```
public Object getEntity(Node node)
```


返回一个不透明的位置[LayoutEnumerator](../../com.aspose.words/layoutenumerator)它对应于指定的节点。您可以使用返回值作为参数[LayoutEnumerator.getCurrent()](../../com.aspose.words/layoutenumerator\#getCurrent--) / [LayoutEnumerator.setCurrent(java.lang.Object)](../../com.aspose.words/layoutenumerator\#setCurrent-java.lang.Object-)给定被枚举的文档和节点的文档是相同的。

此方法仅适用于[Paragraph](../../com.aspose.words/paragraph)节点，以及不可分割的内联节点，例如[BookmarkStart](../../com.aspose.words/bookmarkstart)或者[Shape](../../com.aspose.words/shape).它不适用于[Run](../../com.aspose.words/run), [Cell](../../com.aspose.words/cell) [Row](../../com.aspose.words/row)或者[Table](../../com.aspose.words/table)节点，以及页眉/页脚中的节点。

请注意，为 a 返回的实体[Paragraph](../../com.aspose.words/paragraph)节点是一个分段跨度。使用适当的方法提升到父行

如果您需要导航到[Run](../../com.aspose.words/run)文本然后您可以在它之前插入书签，然后导航到书签。

如果您需要导航到[Cell](../../com.aspose.words/cell)节点然后你可以移动到一个[Paragraph](../../com.aspose.words/paragraph)此单元格中的节点，然后上升到父实体。相同的方法可用于[Row](../../com.aspose.words/row)和[Table](../../com.aspose.words/table)节点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) |  |

**退货:**
java.lang.Object
### getNumPagesSpanned(Node node) {#getNumPagesSpanned-com.aspose.words.Node-}
```
public int getNumPagesSpanned(Node node)
```


获取指定节点跨越的页数。如果节点在单个页面内，则为 0。这与[getEndPageIndex(com.aspose.words.Node)](../../com.aspose.words/layoutcollector\#getEndPageIndex-com.aspose.words.Node-) -[getStartPageIndex(com.aspose.words.Node)](../../com.aspose.words/layoutcollector\#getStartPageIndex-com.aspose.words.Node-).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) |  |

**退货:**
整数
### getStartPageIndex(Node node) {#getStartPageIndex-com.aspose.words.Node-}
```
public int getStartPageIndex(Node node)
```


获取节点开始的页面的从 1 开始的索引。如果节点无法映射到页面，则返回 0。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) |  |

**退货:**
整数
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




### setDocument(Document value) {#setDocument-com.aspose.words.Document-}
```
public void setDocument(Document value)
```


设置此收集器实例附加到的文档。如果您需要访问文档节点的页面索引，则需要在构建文档的页面布局之前将此属性设置为指向文档实例。最好在之后将此属性设置为 null，否则收集器会继续从文档页面布局的后续重建中积累信息。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [Document](../../com.aspose.words/document) | 此收集器实例附加到的文档。 |

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
