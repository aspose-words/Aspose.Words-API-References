---
title: BookmarkCollection
second_title: Aspose.Words for Java API 参考
description: 表示指定范围内的书签的对象集合。
type: docs
weight: 32
url: /zh/java/com.aspose.words/bookmarkcollection/
---

**遗产：**
java.lang.Object

**所有已实现的接口：**
java.lang.Iterable
```
public class BookmarkCollection implements Iterable
```

的集合[Bookmark](../../com.aspose.words/bookmark)表示指定范围内书签的对象。

要了解更多信息，请访问**Working with Bookmarks**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [clear()](#clear--) | 从此集合和文档中删除所有书签。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 返回指定索引处的书签。 |
| [get(String bookmarkName)](#get-java.lang.String-) | 按名称返回书签。 |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | 返回集合中的书签数。 |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | 返回一个枚举器对象。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(Bookmark bookmark)](#remove-com.aspose.words.Bookmark-) | 从文档中删除指定的书签。 |
| [remove(String bookmarkName)](#remove-java.lang.String-) | 删除具有指定名称的书签。 |
| [removeAt(int index)](#removeAt-int-) | 删除指定索引处的书签。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clear() {#clear--}
```
public void clear()
```


从此集合和文档中删除所有书签。

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
public Bookmark get(int index)
```


返回指定索引处的书签。

该指数是从零开始的。

允许使用负索引，表示从集合的后面访问。例如 -1 表示最后一项，-2 表示倒数第二项，依此类推。

如果索引大于或等于列表中的项目数，则返回空引用。

如果索引为负且其绝对值大于列表中的项目数，则返回空引用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 集合中的索引。 |

**退货：**
[Bookmark](../../com.aspose.words/bookmark) 指定索引处的书签。
### get(String bookmarkName) {#get-java.lang.String-}
```
public Bookmark get(String bookmarkName)
```


按名称返回书签。

如果找不到具有指定名称的书签，则返回 null。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | java.lang.String | 书签名称不区分大小写。 |

**退货：**
[Bookmark](../../com.aspose.words/bookmark) - 书签名称。
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


返回集合中的书签数。

**退货：**
int - 集合中书签的数量。
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




### remove(Bookmark bookmark) {#remove-com.aspose.words.Bookmark-}
```
public void remove(Bookmark bookmark)
```


从文档中删除指定的书签。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmark | [Bookmark](../../com.aspose.words/bookmark) | 要删除的书签。 |

### remove(String bookmarkName) {#remove-java.lang.String-}
```
public void remove(String bookmarkName)
```


删除具有指定名称的书签。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | java.lang.String | 要删除的书签的名称不区分大小写。 |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


删除指定索引处的书签。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 要删除的书签的从零开始的索引。 |

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
