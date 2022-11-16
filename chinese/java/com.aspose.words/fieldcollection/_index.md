---
title: FieldCollection
second_title: Aspose.Words for Java API 参考
description: 表示指定范围内的字段的对象集合。
type: docs
weight: 169
url: /zh/java/com.aspose.words/fieldcollection/
---

**遗产：**
java.lang.Object

**所有已实现的接口：**
java.lang.Iterable
```
public class FieldCollection implements Iterable
```

的集合[Field](../../com.aspose.words/field)表示指定范围内的字段的对象。

要了解更多信息，请访问**Working with Fields**文档文章。

此集合的一个实例迭代开始落在指定范围内的字段。

这[FieldCollection](../../com.aspose.words/fieldcollection)集合不拥有它包含的字段，而只是字段的选择。

这[FieldCollection](../../com.aspose.words/fieldcollection)集合是“实时的”，即对创建它的节点对象的子对象的更改会立即反映在由[FieldCollection](../../com.aspose.words/fieldcollection)属性和方法。
## 方法

| 方法 | 描述 |
| --- | --- |
| [clear()](#clear--) | 从文档和此集合本身中删除此集合的所有字段。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 返回指定索引处的字段。 |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | 返回集合中的字段数。 |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | 返回一个枚举器对象。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(Field field)](#remove-com.aspose.words.Field-) | 从此集合和文档中删除指定的字段。 |
| [removeAt(int index)](#removeAt-int-) | 从此集合和文档中删除指定索引处的字段。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clear() {#clear--}
```
public void clear()
```


从文档和此集合本身中删除此集合的所有字段。

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
public Field get(int index)
```


返回指定索引处的字段。

该指数是从零开始的。

允许使用负索引，表示从集合的后面访问。例如 -1 表示最后一项，-2 表示倒数第二项，依此类推。

如果索引大于或等于列表中的项目数，则返回空引用。

如果索引为负且其绝对值大于列表中的项目数，则返回空引用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 集合中的索引。 |

**退货：**
[Field](../../com.aspose.words/field) - 指定索引处的字段。
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


返回集合中的字段数。

**退货：**
int - 集合中的字段数。
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




### remove(Field field) {#remove-com.aspose.words.Field-}
```
public void remove(Field field)
```


从此集合和文档中删除指定的字段。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field) | 要删除的字段。 |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


从此集合和文档中删除指定索引处的字段。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 集合中的索引。 |

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
