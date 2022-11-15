---
title: VariableCollection
second_title: Aspose.Words for Java API 参考
description: 文档变量的集合。
type: docs
weight: 592
url: /zh/java/com.aspose.words/variablecollection/
---

**遗产：**
java.lang.Object

**所有已实现的接口：**
java.lang.Iterable
```
public class VariableCollection implements Iterable
```

文档变量的集合。

要了解更多信息，请访问**Work with Document Properties**文档文章。

变量名和值是字符串。

变量名称不区分大小写。
## 方法

| 方法 | 描述 |
| --- | --- |
| [add(String name, String value)](#add-java.lang.String-java.lang.String-) | 将文档变量添加到集合中。 |
| [clear()](#clear--) | 从集合中移除所有元素。 |
| [contains(String name)](#contains-java.lang.String-) | 确定集合是否包含具有给定名称的文档变量。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 获取指定索引处的文档变量。 |
| [get(String name)](#get-java.lang.String-) | 提供对集合项的访问。 |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | 获取集合中包含的元素数。 |
| [hashCode()](#hashCode--) |  |
| [indexOfKey(String name)](#indexOfKey-java.lang.String-) | 返回集合中指定文档变量的从零开始的索引。 |
| [iterator()](#iterator--) | 返回一个枚举器对象，该对象可用于迭代集合中的所有变量。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(String name)](#remove-java.lang.String-) | 从集合中移除具有指定名称的文档变量。 |
| [removeAt(int index)](#removeAt-int-) | 删除指定索引处的文档变量。 |
| [set(int index, String value)](#set-int-java.lang.String-) | 在指定索引处设置文档变量。 |
| [set(String name, String value)](#set-java.lang.String-java.lang.String-) | 提供对集合项的访问。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(String name, String value) {#add-java.lang.String-java.lang.String-}
```
public void add(String name, String value)
```


将文档变量添加到集合中。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 要添加的变量的名称不区分大小写。 |
| value | java.lang.String | 变量的值。该值不能为空，如果值为空，将使用空字符串代替。 |

### clear() {#clear--}
```
public void clear()
```


从集合中移除所有元素。

### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


确定集合是否包含具有给定名称的文档变量。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 要定位的文档变量的名称不区分大小写。 |

**退货：**
boolean - 如果在集合中找到项目，则为真；否则，假的。
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
public String get(int index)
```


获取指定索引处的文档变量。空值不允许作为赋值的右侧，将被空字符串替换。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 文档变量的从零开始的索引。 |

**退货：**
java.lang.String - 指定索引处的文档变量。
### get(String name) {#get-java.lang.String-}
```
public String get(String name)
```


提供对集合项的访问。通过不区分大小写的名称获取或设置文档变量。空值不允许作为赋值的右侧，将被空字符串替换。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String |  |

**退货：**
java.lang.String - 相应的 java.lang.String 值。
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


获取集合中包含的元素数。

**退货：**
int - 集合中包含的元素数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### indexOfKey(String name) {#indexOfKey-java.lang.String-}
```
public int indexOfKey(String name)
```


返回集合中指定文档变量的从零开始的索引。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 变量的名称不区分大小写。 |

**退货：**
int - 从零开始的索引。如果未找到，则为负值。
### iterator() {#iterator--}
```
public Iterator iterator()
```


返回一个枚举器对象，该对象可用于迭代集合中的所有变量。

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




### remove(String name) {#remove-java.lang.String-}
```
public void remove(String name)
```


从集合中移除具有指定名称的文档变量。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 变量的名称不区分大小写。 |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


删除指定索引处的文档变量。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 从零开始的索引。 |

### set(int index, String value) {#set-int-java.lang.String-}
```
public void set(int index, String value)
```


在指定索引处设置文档变量。空值不允许作为赋值的右侧，将被空字符串替换。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 文档变量的从零开始的索引。 |
| value | java.lang.String | 指定索引处的文档变量。 |

### set(String name, String value) {#set-java.lang.String-java.lang.String-}
```
public void set(String name, String value)
```


提供对集合项的访问。通过不区分大小写的名称获取或设置文档变量。空值不允许作为赋值的右侧，将被空字符串替换。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String |  |
| value | java.lang.String | 对应的java.lang.String值。 |

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
