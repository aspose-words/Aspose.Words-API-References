---
title: CustomPartCollection
second_title: Aspose.Words for Java API 参考
description: 表示对象的集合。
type: docs
weight: 103
url: /zh/java/com.aspose.words/custompartcollection/
---

**遗产：**
java.lang.Object

**所有已实现的接口：**
java.lang.Iterable
```
public class CustomPartCollection implements Iterable
```

代表集合[CustomPart](../../com.aspose.words/custompart)对象。

要了解更多信息，请访问**Structured Document Tags or Content Control**文档文章。

您通常不需要创建此类的实例。您可以通过以下方式访问与 OOXML 包相关的自定义部分[Document.getPackageCustomParts()](../../com.aspose.words/document\#getPackageCustomParts--) / [Document.setPackageCustomParts(com.aspose.words.CustomPartCollection)](../../com.aspose.words/document\#setPackageCustomParts-com.aspose.words.CustomPartCollection-)财产。
## 方法

| 方法 | 描述 |
| --- | --- |
| [add(CustomPart part)](#add-com.aspose.words.CustomPart-) | 将项目添加到集合中。 |
| [clear()](#clear--) | 从集合中移除所有元素。 |
| [deepClone()](#deepClone--) | 制作此集合及其项目的深层副本。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 获取指定索引处的项目。 |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | 获取集合中包含的元素数。 |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | 返回一个迭代器对象，该对象可用于迭代集合中的所有项目。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeAt(int index)](#removeAt-int-) | 删除指定索引处的项目。 |
| [set(int index, CustomPart value)](#set-int-com.aspose.words.CustomPart-) | 在指定的索引处设置一个项目。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(CustomPart part) {#add-com.aspose.words.CustomPart-}
```
public void add(CustomPart part)
```


将项目添加到集合中。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| part | [CustomPart](../../com.aspose.words/custompart) | 要添加的项目。 |

### clear() {#clear--}
```
public void clear()
```


从集合中移除所有元素。

### deepClone() {#deepClone--}
```
public CustomPartCollection deepClone()
```


制作此集合及其项目的深层副本。

**退货：**
[CustomPartCollection](../../com.aspose.words/custompartcollection)
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
public CustomPart get(int index)
```


获取指定索引处的项目。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 项目的从零开始的索引。 |

**退货：**
[CustomPart](../../com.aspose.words/custompart) - 指定索引处的项目。
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
### iterator() {#iterator--}
```
public Iterator iterator()
```


返回一个迭代器对象，该对象可用于迭代集合中的所有项目。

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




### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


删除指定索引处的项目。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 从零开始的索引。 |

### set(int index, CustomPart value) {#set-int-com.aspose.words.CustomPart-}
```
public void set(int index, CustomPart value)
```


在指定的索引处设置一个项目。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 项目的从零开始的索引。 |
| value | [CustomPart](../../com.aspose.words/custompart) | 指定索引处的项目。 |

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
