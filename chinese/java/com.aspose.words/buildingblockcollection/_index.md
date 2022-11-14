---
title: BuildingBlockCollection
second_title: Aspose.Words for Java API 参考
description: 文档中的对象集合。
type: docs
weight: 43
url: /zh/java/com.aspose.words/buildingblockcollection/
---

**遗产:**
java.lang.Object, [com.aspose.words.NodeCollection](../../com.aspose.words/nodecollection)
```
public class BuildingBlockCollection extends NodeCollection
```

的集合[BuildingBlock](../../com.aspose.words/buildingblock)文档中的对象。

要了解更多信息，请访问**Aspose.Words Document Object Model (DOM)**文档文章。

您不直接创建此类的实例。要访问构建块的集合，请使用[GlossaryDocument.getBuildingBlocks()](../../com.aspose.words/glossarydocument\#getBuildingBlocks--)财产。
## 方法

| 方法 | 描述 |
| --- | --- |
| [add(Node node)](#add-com.aspose.words.Node-) | 将节点添加到集合的末尾。 |
| [clear()](#clear--) | 从此集合和文档中删除所有节点。 |
| [contains(Node node)](#contains-com.aspose.words.Node-) | 确定节点是否在集合中。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 在给定索引处检索构建块。 |
| [getClass()](#getClass--) |  |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | 获取集合中的节点数。 |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [hashCode()](#hashCode--) |  |
| [indexOf(Node node)](#indexOf-com.aspose.words.Node-) | 返回指定节点的从零开始的索引。 |
| [insert(int index, Node node)](#insert-int-com.aspose.words.Node-) | 将节点插入到集合中指定索引处。 |
| [iterator()](#iterator--) | 在节点集合上提供简单的“foreach”样式迭代。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(Node node)](#remove-com.aspose.words.Node-) | 从集合和文档中删除节点。 |
| [removeAt(int index)](#removeAt-int-) | 从集合和文档中删除指定索引处的节点。 |
| [toArray()](#toArray--) | 将集合中的所有构建块复制到新的构建块数组中。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(Node node) {#add-com.aspose.words.Node-}
```
public void add(Node node)
```


将节点添加到集合的末尾。

该节点作为子节点插入到从中创建集合的节点对象中。

如果 newChild 已经在树中，则首先将其移除。

如果要插入的节点是从另一个文档创建的，您应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) | 要添加到集合末尾的节点。 |

### clear() {#clear--}
```
public void clear()
```


从此集合和文档中删除所有节点。

### contains(Node node) {#contains-com.aspose.words.Node-}
```
public boolean contains(Node node)
```


确定节点是否在集合中。

该方法执行线性搜索；因此，平均执行时间与 Count 成正比。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) | 要定位的节点。 |

**退货:**
boolean - 如果在集合中找到项目，则为真；否则为假。
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
public Node get(int index)
```


在给定索引处检索构建块。

该指数是从零开始的。

允许使用负索引，表示从集合的后面访问。例如 -1 表示最后一项，-2 表示倒数第二项，依此类推。

如果索引大于或等于列表中的项目数，则返回空引用。

如果索引为负且其绝对值大于列表中的项目数，则返回空引用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 构建块列表的索引。 |

**退货:**
[Node](../../com.aspose.words/node) - 相应的[BuildingBlock](../../com.aspose.words/buildingblock)价值。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getContainer() {#getContainer--}
```
public CompositeNode getContainer()
```




**退货:**
[CompositeNode](../../com.aspose.words/compositenode)
### getCount() {#getCount--}
```
public int getCount()
```


获取集合中的节点数。

**退货:**
int - 集合中的节点数。
### getCurrentNode() {#getCurrentNode--}
```
public Node getCurrentNode()
```




**退货:**
[Node](../../com.aspose.words/node)
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node-}
```
public Node getNextMatchingNode(Node curNode)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node) |  |

**退货:**
[Node](../../com.aspose.words/node)
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### indexOf(Node node) {#indexOf-com.aspose.words.Node-}
```
public int indexOf(Node node)
```


返回指定节点的从零开始的索引。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) | 要定位的节点。 |

**退货:**
int - 集合中节点的从零开始的索引（如果找到）；否则，-1。

该方法执行线性搜索；因此，平均执行时间与 Count 成正比。
### insert(int index, Node node) {#insert-int-com.aspose.words.Node-}
```
public void insert(int index, Node node)
```


将节点插入到集合中指定索引处。

该节点作为子节点插入到从中创建集合的节点对象中。

如果索引等于或大于 Count，则将节点添加到集合的末尾。

如果索引为负且其绝对值大于 Count，则将节点添加到集合的末尾。

如果 newChild 已经在树中，则首先将其移除。

如果要插入的节点是从另一个文档创建的，您应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 节点的从零开始的索引。允许使用负索引并指示从列表后面进行访问。例如 -1 表示最后一个节点，-2 表示倒数第二个，依此类推。 |
| node | [Node](../../com.aspose.words/node) | 要插入的节点。 |

### iterator() {#iterator--}
```
public Iterator iterator()
```


在节点集合上提供简单的“foreach”样式迭代。

**退货:**
java.util.Iterator - 一个迭代器。
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### remove(Node node) {#remove-com.aspose.words.Node-}
```
public void remove(Node node)
```


从集合和文档中删除节点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) | 要移除的节点。 |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


从集合和文档中删除指定索引处的节点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 节点的从零开始的索引。允许使用负索引并指示从列表后面进行访问。例如 -1 表示最后一个节点，-2 表示倒数第二个，依此类推。 |

### toArray() {#toArray--}
```
public Node[] toArray()
```


将集合中的所有构建块复制到新的构建块数组中。

**退货:**
com.aspose.words.Node[] - 一组构建块。
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
