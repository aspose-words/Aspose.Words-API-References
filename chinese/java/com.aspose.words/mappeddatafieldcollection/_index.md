---
title: MappedDataFieldCollection
second_title: Aspose.Words for Java API 参考
description: 允许在数据源中的字段名称和文档中的邮件合并字段名称之间自动映射。
type: docs
weight: 387
url: /zh/java/com.aspose.words/mappeddatafieldcollection/
---

**遗产：**
java.lang.Object

**所有已实现的接口：**
java.lang.Iterable
```
public class MappedDataFieldCollection implements Iterable
```

允许在数据源中的字段名称和文档中的邮件合并字段名称之间自动映射。

要了解更多信息，请访问**Mail Merge and Reporting**文档文章。

这是作为字符串键到字符串值的集合来实现的。键是文档中邮件合并字段的名称，值是数据源中字段的名称。
## 方法

| 方法 | 描述 |
| --- | --- |
| [add(String documentFieldName, String dataSourceFieldName)](#add-java.lang.String-java.lang.String-) | 添加新的字段映射。 |
| [clear()](#clear--) | 从集合中移除所有元素。 |
| [containsKey(String documentFieldName)](#containsKey-java.lang.String-) | 确定文档中指定字段的映射是否存在于集合中。 |
| [containsValue(String dataSourceFieldName)](#containsValue-java.lang.String-) | 确定集合中是否存在来自数据源中指定字段的映射。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(String documentFieldName)](#get-java.lang.String-) | 获取数据源中与指定邮件合并字段关联的字段名称。 |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | 获取集合中包含的元素数。 |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | 返回一个字典迭代器对象，可用于迭代集合中的所有项目。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(String documentFieldName)](#remove-java.lang.String-) | 删除字段映射。 |
| [set(String documentFieldName, String value)](#set-java.lang.String-java.lang.String-) | 设置与指定邮件合并字段关联的数据源中的字段名称。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(String documentFieldName, String dataSourceFieldName) {#add-java.lang.String-java.lang.String-}
```
public void add(String documentFieldName, String dataSourceFieldName)
```


添加新的字段映射。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| documentFieldName | java.lang.String | 文档中邮件合并字段的区分大小写的名称。 |
| dataSourceFieldName | java.lang.String | 数据源中字段的区分大小写的名称。 |

### clear() {#clear--}
```
public void clear()
```


从集合中移除所有元素。

### containsKey(String documentFieldName) {#containsKey-java.lang.String-}
```
public boolean containsKey(String documentFieldName)
```


确定文档中指定字段的映射是否存在于集合中。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| documentFieldName | java.lang.String | 文档中邮件合并字段的区分大小写的名称。 |

**退货：**
boolean - 如果在集合中找到项目，则为真；否则，假的。
### containsValue(String dataSourceFieldName) {#containsValue-java.lang.String-}
```
public boolean containsValue(String dataSourceFieldName)
```


确定集合中是否存在来自数据源中指定字段的映射。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataSourceFieldName | java.lang.String | 数据源中字段的区分大小写的名称。 |

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
### get(String documentFieldName) {#get-java.lang.String-}
```
public String get(String documentFieldName)
```


获取数据源中与指定邮件合并字段关联的字段名称。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| documentFieldName | java.lang.String |  |

**退货：**
java.lang.String - 数据源中与指定邮件合并字段关联的字段名称。
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


返回一个字典迭代器对象，可用于迭代集合中的所有项目。

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




### remove(String documentFieldName) {#remove-java.lang.String-}
```
public void remove(String documentFieldName)
```


删除字段映射。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| documentFieldName | java.lang.String | 文档中邮件合并字段的区分大小写的名称。 |

### set(String documentFieldName, String value) {#set-java.lang.String-java.lang.String-}
```
public void set(String documentFieldName, String value)
```


设置与指定邮件合并字段关联的数据源中的字段名称。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| documentFieldName | java.lang.String |  |
| value | java.lang.String | 数据源中与指定邮件合并字段关联的字段名称。 |

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
