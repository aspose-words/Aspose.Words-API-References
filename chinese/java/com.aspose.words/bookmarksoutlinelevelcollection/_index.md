---
title: BookmarksOutlineLevelCollection
second_title: Aspose.Words for Java API 参考
description:单个书签大纲级别的集合。
type: docs
weight: 35
url: /zh/java/com.aspose.words/bookmarksoutlinelevelcollection/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Iterable
```
public class BookmarksOutlineLevelCollection implements Iterable
```

单个书签大纲级别的集合。

要了解更多信息，请访问**Working with Bookmarks**文档文章。

Key 是不区分大小写的字符串书签名称。值是一个 int 书签大纲级别。

书签大纲级别可以是 0 到 9 之间的值。指定 0 并且 Word 书签将不会显示在文档大纲中。指定 1，Word 书签将显示在第 1 级的文档大纲中； 2 表示 2 级，依此类推。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [add(String name, int outlineLevel)](#add-java.lang.String-int-) | 将书签添加到集合中。 |
| [clear()](#clear--) | 从集合中移除所有元素。 |
| [contains(String name)](#contains-java.lang.String-) | 确定集合是否包含具有给定名称的书签。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 获取指定索引处的书签大纲级别。 |
| [get(String name)](#get-java.lang.String-) | 提供对集合项目的访问。 |
| [get班级()](#get班级--) |  |
| [getCount()](#getCount--) | 获取集合中包含的元素数。 |
| [hashCode()](#hashCode--) |  |
| [indexOfKey(String name)](#indexOfKey-java.lang.String-) | 返回集合中指定书签的从零开始的索引。 |
| [iterator()](#iterator--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(String name)](#remove-java.lang.String-) | 从集合中删除具有指定名称的书签。 |
| [removeAt(int index)](#removeAt-int-) | 删除指定索引处的书签。 |
| [set(int index, int value)](#set-int-int-) | 在指定索引处设置书签大纲级别。 |
| [set(String name, int value)](#set-java.lang.String-int-) | 提供对集合项目的访问。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(String name, int outlineLevel) {#add-java.lang.String-int-}
```
public void add(String name, int outlineLevel)
```


将书签添加到集合中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 要添加的书签的不区分大小写的名称。 |
| outlineLevel | int | 书签的大纲级别。有效范围是 0 到 9。 |

### clear() {#clear--}
```
public void clear()
```


从集合中移除所有元素。

### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


确定集合是否包含具有给定名称的书签。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 要查找的书签的不区分大小写的名称。 |

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
public int get(int index)
```


获取指定索引处的书签大纲级别。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 书签的从零开始的索引。 |

**退货:**
int - 书签的大纲级别。有效范围是 0 到 9。
### get(String name) {#get-java.lang.String-}
```
public int get(String name)
```


提供对集合项目的访问。通过书签名称获取或设置书签大纲级别。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 不区分大小写的书签名称。 |

**退货:**
int - 书签的大纲级别。有效范围是 0 到 9。
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


获取集合中包含的元素数。

**退货:**
int - 集合中包含的元素数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### indexOfKey(String name) {#indexOfKey-java.lang.String-}
```
public int indexOfKey(String name)
```


返回集合中指定书签的从零开始的索引。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 书签的不区分大小写的名称。 |

**退货:**
int - 从零开始的索引。如果未找到，则为负值。
### iterator() {#iterator--}
```
public Iterator iterator()
```




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




### remove(String name) {#remove-java.lang.String-}
```
public void remove(String name)
```


从集合中删除具有指定名称的书签。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 书签的不区分大小写的名称。 |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


删除指定索引处的书签。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 从零开始的索引。 |

### set(int index, int value) {#set-int-int-}
```
public void set(int index, int value)
```


在指定索引处设置书签大纲级别。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 书签的从零开始的索引。 |
| value | int | 书签的大纲级别。有效范围是 0 到 9。 |

### set(String name, int value) {#set-java.lang.String-int-}
```
public void set(String name, int value)
```


提供对集合项目的访问。通过书签名称获取或设置书签大纲级别。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 不区分大小写的书签名称。 |
| value | int | 书签的大纲级别。有效范围是 0 到 9。 |

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
