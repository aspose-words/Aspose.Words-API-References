---
title: Form字段Collection
second_title: Aspose.Words for Java API Reference
description: 代表范围内所有表单字段的 Form字段 对象的集合。
type: docs
weight: 297
url: /zh/java/com.aspose.words/formfieldcollection/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Iterable
```
public class Form字段Collection implements Iterable
```

一个集合**Form字段**表示范围内所有表单域的对象。

要了解更多信息，请访问**Working with Form 字段**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [clear()](#clear--) | 从此集合和文档中删除所有表单域。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 返回指定索引处的表单字段。 |
| [get(String bookmarkName)](#get-java.lang.String-) | 按书签名称返回表单字段。 |
| [get班级()](#get班级--) |  |
| [getCount()](#getCount--) | 返回集合中表单域的数量。 |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | 返回一个枚举器对象。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(String form字段)](#remove-java.lang.String-) | 删除具有指定名称的表单域。 |
| [removeAt(int index)](#removeAt-int-) | 删除指定索引处的表单域。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clear() {#clear--}
```
public void clear()
```


从此集合和文档中删除所有表单域。

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
public Form字段 get(int index)
```


返回指定索引处的表单字段。

该索引从零开始。

允许使用负索引并指示从集合的背面进行访问。例如 -1 表示最后一项，-2 表示倒数第二个，依此类推。

如果 index 大于或等于列表中的项目数，则返回空引用。

如果 index 为负且其绝对值大于列表中的项目数，则返回空引用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 集合中的索引。 |

**退货:**
[Form字段](../../com.aspose.words/formfield) - 指定索引处的表单域。
### get(String bookmarkName) {#get-java.lang.String-}
```
public Form字段 get(String bookmarkName)
```


按书签名称返回表单字段。如果找不到具有指定书签名称的表单字段，则返回 null。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | java.lang.String | 不区分大小写的书签名称。 |

**退货:**
[Form字段](../../com.aspose.words/formfield) - 书签名称的表单字段。
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


返回集合中表单域的数量。

**退货:**
int - 集合中的表单字段数。
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


返回一个枚举器对象。

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




### remove(String form字段) {#remove-java.lang.String-}
```
public void remove(String form字段)
```


删除具有指定名称的表单域。如果存在与表单域关联的书签，则不会删除该书签。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| form字段 | java.lang.String | 要删除的表单字段的不区分大小写的名称。 |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


删除指定索引处的表单域。如果存在与表单域关联的书签，则不会删除该书签。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 要删除的表单字段的从零开始的索引。 |

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
