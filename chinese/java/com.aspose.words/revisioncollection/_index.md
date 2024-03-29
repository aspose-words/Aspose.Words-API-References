---
title: RevisionCollection
second_title: Aspose.Words for Java API 参考
description: 代表文档中修订的对象集合。
type: docs
weight: 484
url: /zh/java/com.aspose.words/revisioncollection/
---

**遗产：**
java.lang.Object

**所有已实现的接口：**
java.lang.Iterable
```
public class RevisionCollection implements Iterable
```

的集合[Revision](../../com.aspose.words/revision)表示文档修订的对象。

要了解更多信息，请访问**Track Changes in a Document**文档文章。

您不直接创建此类的实例。使用[Document.getRevisions()](../../com.aspose.words/document\#getRevisions--)属性来获取文档中存在的修订。
## 方法

| 方法 | 描述 |
| --- | --- |
| [acceptAll()](#acceptAll--) | 接受此集合中的所有修订。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 返回指定索引处的修订。 |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | 返回集合中的修订数。 |
| [getGroups()](#getGroups--) | 修订组的集合。 |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | 返回一个枚举器对象。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [rejectAll()](#rejectAll--) | 拒绝此集合中的所有修订。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### acceptAll() {#acceptAll--}
```
public void acceptAll()
```


接受此集合中的所有修订。

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
### get(int index) {#get-int-}
```
public Revision get(int index)
```


返回指定索引处的修订。

该指数是从零开始的。

允许使用负索引，表示从集合的后面访问。例如 -1 表示最后一项，-2 表示倒数第二项，依此类推。

如果索引大于或等于列表中的项目数，则返回空引用。

如果索引为负且其绝对值大于列表中的项目数，则返回空引用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 集合中的索引。 |

**退货：**
[Revision](../../com.aspose.words/revision) - 指定索引处的修订。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getCount() {#getCount--}
```
public int getCount()
```


返回集合中的修订数。

**退货：**
int - 集合中的修订数。
### getGroups() {#getGroups--}
```
public RevisionGroupCollection getGroups()
```


修订组的集合。

**退货：**
[RevisionGroupCollection](../../com.aspose.words/revisiongroupcollection) - 相应的[RevisionGroupCollection](../../com.aspose.words/revisiongroupcollection)价值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### iterator() {#iterator--}
```
public Iterator iterator()
```


返回一个枚举器对象。

**退货：**
java.util.迭代器
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### rejectAll() {#rejectAll--}
```
public void rejectAll()
```


拒绝此集合中的所有修订。

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
