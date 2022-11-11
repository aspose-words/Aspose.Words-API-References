---
title: DocumentPropertyCollection
second_title: Aspose.Words for Java API 参考
description:和集合的基类。
type: docs
weight: 127
url: /zh/java/com.aspose.words/documentpropertycollection/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Iterable
```
public abstract class DocumentPropertyCollection implements Iterable
```

基类[BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties)和[CustomDocumentProperties](../../com.aspose.words/customdocumentproperties)收藏品。

要了解更多信息，请访问**Work with Document Properties**文档文章。

属性名称不区分大小写。

集合中的属性按名称的字母顺序排序。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [DocumentPropertyCollection()](#DocumentPropertyCollection--) |  |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [clear()](#clear--) | 从集合中删除所有属性。 |
| [contains(String name)](#contains-java.lang.String-) | 如果集合中存在具有指定名称的属性，则返回 true。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 返回一个[DocumentProperty](../../com.aspose.words/documentproperty)按索引的对象。 |
| [get(String name)](#get-java.lang.String-) | 提供对集合项目的访问。 |
| [get班级()](#get班级--) |  |
| [getCount()](#getCount--) | 获取集合中的项目数。 |
| [hashCode()](#hashCode--) |  |
| [indexOf(String name)](#indexOf-java.lang.String-) | 按名称获取属性的索引。 |
| [iterator()](#iterator--) | 返回一个迭代器对象，该对象可用于迭代集合中的所有项目。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(String name)](#remove-java.lang.String-) | 从集合中移除具有指定名称的属性。 |
| [removeAt(int index)](#removeAt-int-) | 删除指定索引处的属性。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DocumentPropertyCollection() {#DocumentPropertyCollection--}
```
public DocumentPropertyCollection()
```


### clear() {#clear--}
```
public void clear()
```


从集合中删除所有属性。

### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


如果集合中存在具有指定名称的属性，则返回 true。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 不区分大小写的属性名称。 |

**退货:**
boolean - 如果属性存在于集合中，则为真；否则为假。
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
public DocumentProperty get(int index)
```


返回一个[DocumentProperty](../../com.aspose.words/documentproperty)按索引的对象。

**Note:**在 Java 中，这种方法很慢，因为它会遍历所有节点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 的从零开始的索引[DocumentProperty](../../com.aspose.words/documentproperty)检索。 |

**退货:**
[DocumentProperty](../../com.aspose.words/documentproperty) - 一个[DocumentProperty](../../com.aspose.words/documentproperty)按索引的对象。
### get(String name) {#get-java.lang.String-}
```
public DocumentProperty get(String name)
```


提供对集合项目的访问。返回一个[DocumentProperty](../../com.aspose.words/documentproperty)对象的属性名称。

如果未找到具有指定名称的属性，则返回 null。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 要检索的属性的不区分大小写的名称。 |

**退货:**
[DocumentProperty](../../com.aspose.words/documentproperty) - 相应的[DocumentProperty](../../com.aspose.words/documentproperty)价值。
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


获取集合中的项目数。

**退货:**
int - 集合中的项目数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### indexOf(String name) {#indexOf-java.lang.String-}
```
public int indexOf(String name)
```


按名称获取属性的索引。

**Note:**在 Java 中，这种方法很慢，因为它会遍历所有节点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 不区分大小写的属性名称。 |

**退货:**
int - 从零开始的索引。如果未找到，则为负值。
### iterator() {#iterator--}
```
public Iterator iterator()
```


返回一个迭代器对象，该对象可用于迭代集合中的所有项目。

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


从集合中移除具有指定名称的属性。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 不区分大小写的属性名称。 |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


删除指定索引处的属性。

**Note:**在 Java 中，这种方法很慢，因为它会遍历所有节点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 从零开始的索引。 |

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
