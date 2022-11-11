---
title: NodeList
second_title: Aspose.Words for Java API Reference
description: 表示与使用该方法执行的 XPath 查询匹配的节点集合。
type: docs
weight: 406
url: /zh/java/com.aspose.words/nodelist/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Iterable
```
public class NodeList implements Iterable
```

表示与使用执行的 XPath 查询匹配的节点集合[CompositeNode.selectNodes(java.lang.String)](../../com.aspose.words/compositenode\#selectNodes-java.lang.String-)方法。

要了解更多信息，请访问**Aspose.Words Document Object Model (DOM)**文档文章。

**NodeList**由返回[CompositeNode.selectNodes(java.lang.String)](../../com.aspose.words/compositenode\#selectNodes-java.lang.String-)并包含与 XPath 查询匹配的节点集合。

**NodeList**支持索引访问和迭代。

对待**NodeList**集合作为“快照”集合。**NodeList**以“实时”集合开始，因为在运行 XPath 查询时实际上并未检索到节点。节点仅在访问时被检索，此时节点和它之前的所有节点都被缓存，形成一个“快照”集合。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 检索给定索引处的节点。 |
| [get班级()](#get班级--) |  |
| [getCount()](#getCount--) | 获取列表中的节点数。 |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | 在节点集合上提供简单的“foreach”样式迭代。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toArray()](#toArray--) | 将集合中的所有节点复制到新的节点数组。 |
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
public Node get(int index)
```


检索给定索引处的节点。

该索引从零开始。

允许使用负索引并指示从集合的背面进行访问。例如 -1 表示最后一项，-2 表示倒数第二个，依此类推。

如果 index 大于或等于列表中的项目数，则返回空引用。

如果 index 为负且其绝对值大于列表中的项目数，则返回空引用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 节点列表的索引。 |

**退货:**
[Node](../../com.aspose.words/node) - 相应的[Node](../../com.aspose.words/node)价值。
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


获取列表中的节点数。

**退货:**
int - 列表中的节点数。
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




### toArray() {#toArray--}
```
public Node[] toArray()
```


将集合中的所有节点复制到新的节点数组。

您不应该在迭代节点集合时添加/删除节点，因为它会使迭代器无效并且需要刷新实时集合。

为了能够在迭代期间添加/删除节点，请使用此方法将节点复制到固定大小的数组中，然后遍历该数组。

**退货:**
com.aspose.words.Node[] - 一个节点数组。
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
