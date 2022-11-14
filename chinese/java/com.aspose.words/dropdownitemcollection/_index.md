---
title: DropDownItemCollection
second_title: Aspose.Words for Java API 参考
description: 代表下拉表单字段中所有项目的字符串集合。
type: docs
weight: 135
url: /zh/java/com.aspose.words/dropdownitemcollection/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Iterable
```
public class DropDownItemCollection implements Iterable
```

表示下拉表单字段中所有项目的字符串集合。

要了解更多信息，请访问**Working with 字段**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [add(String value)](#add-java.lang.String-) |  |
| [clear()](#clear--) | 从集合中移除所有元素。 |
| [contains(String value)](#contains-java.lang.String-) | 确定集合是否包含指定值。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 获取指定索引处的元素。 |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | 获取集合中包含的元素数。 |
| [hashCode()](#hashCode--) |  |
| [indexOf(String value)](#indexOf-java.lang.String-) | 返回集合中指定值的从零开始的索引。 |
| [insert(int index, String value)](#insert-int-java.lang.String-) | 将字符串插入到指定索引处的集合中。 |
| [isInheritedComplexAttr()](#isInheritedComplexAttr--) |  |
| [iterator()](#iterator--) | 返回一个迭代器对象，该对象可用于迭代集合中的所有项目。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(String name)](#remove-java.lang.String-) | 从集合中移除指定的值。 |
| [removeAt(int index)](#removeAt-int-) | 删除指定索引处的值。 |
| [set(int index, String value)](#set-int-java.lang.String-) | 在指定索引处设置元素。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(String value) {#add-java.lang.String-}
```
public int add(String value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String |  |

**退货:**
整数
### clear() {#clear--}
```
public void clear()
```


从集合中移除所有元素。

### contains(String value) {#contains-java.lang.String-}
```
public boolean contains(String value)
```


确定集合是否包含指定值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 要定位的区分大小写的值。 |

**退货:**
boolean - 如果在集合中找到该项目，则为真；否则为假。
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
public String get(int index)
```


获取指定索引处的元素。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int |  |

**退货:**
java.lang.String - 指定索引处的元素。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
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
### indexOf(String value) {#indexOf-java.lang.String-}
```
public int indexOf(String value)
```


返回集合中指定值的从零开始的索引。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 要定位的区分大小写的值。 |

**退货:**
int - 从零开始的索引。如果未找到，则为负值。
### insert(int index, String value) {#insert-int-java.lang.String-}
```
public void insert(int index, String value)
```


将字符串插入到指定索引处的集合中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 插入值的从零开始的索引。 |
| value | java.lang.String | 要插入的字符串。 |

### isInheritedComplexAttr() {#isInheritedComplexAttr--}
```
public boolean isInheritedComplexAttr()
```




**退货:**
布尔值
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


从集合中移除指定的值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 要删除的区分大小写的值。 |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


删除指定索引处的值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 从零开始的索引。 |

### set(int index, String value) {#set-int-java.lang.String-}
```
public void set(int index, String value)
```


在指定索引处设置元素。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int |  |
| value | java.lang.String | 指定索引处的元素。 |

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
