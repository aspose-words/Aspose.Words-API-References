---
title: MappedData字段Collection
second_title: Aspose.Words for Java API 参考
description:允许在数据源中的字段名称和文档中的邮件合并字段名称之间自动映射。
type: docs
weight: 387
url: /zh/java/com.aspose.words/mappeddatafieldcollection/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Iterable
```
public class MappedData字段Collection implements Iterable
```

允许在数据源中的字段名称和文档中的邮件合并字段名称之间自动映射。

要了解更多信息，请访问**Mail Merge and Reporting**文档文章。

这是作为字符串键的集合实现为字符串值的。键是文档中邮件合并字段的名称，值是数据源中的字段名称。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [add(String document字段Name, String dataSource字段Name)](#add-java.lang.String-java.lang.String-) | 添加新的字段映射。 |
| [clear()](#clear--) | 从集合中移除所有元素。 |
| [containsKey(String document字段Name)](#containsKey-java.lang.String-) | 确定集合中是否存在来自文档中指定字段的映射。 |
| [containsValue(String dataSource字段Name)](#containsValue-java.lang.String-) | 确定集合中是否存在来自数据源中指定字段的映射。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(String document字段Name)](#get-java.lang.String-) | 获取与指定邮件合并字段关联的数据源中的字段名称。 |
| [get班级()](#get班级--) |  |
| [getCount()](#getCount--) | 获取集合中包含的元素数。 |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | 返回一个字典迭代器对象，该对象可用于迭代集合中的所有项目。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(String document字段Name)](#remove-java.lang.String-) | 删除字段映射。 |
| [set(String document字段Name, String value)](#set-java.lang.String-java.lang.String-) | 设置与指定邮件合并字段关联的数据源中的字段名称。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(String document字段Name, String dataSource字段Name) {#add-java.lang.String-java.lang.String-}
```
public void add(String document字段Name, String dataSource字段Name)
```


添加新的字段映射。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document字段Name | java.lang.String | 文档中邮件合并字段的区分大小写的名称。 |
| dataSource字段Name | java.lang.String | 数据源中字段的区分大小写的名称。 |

### clear() {#clear--}
```
public void clear()
```


从集合中移除所有元素。

### containsKey(String document字段Name) {#containsKey-java.lang.String-}
```
public boolean containsKey(String document字段Name)
```


确定集合中是否存在来自文档中指定字段的映射。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document字段Name | java.lang.String | 文档中邮件合并字段的区分大小写的名称。 |

**退货:**
boolean - 如果在集合中找到项目，则为真；否则为假。
### containsValue(String dataSource字段Name) {#containsValue-java.lang.String-}
```
public boolean containsValue(String dataSource字段Name)
```


确定集合中是否存在来自数据源中指定字段的映射。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataSource字段Name | java.lang.String | 数据源中字段的区分大小写的名称。 |

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
### get(String document字段Name) {#get-java.lang.String-}
```
public String get(String document字段Name)
```


获取与指定邮件合并字段关联的数据源中的字段名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document字段Name | java.lang.String |  |

**退货:**
java.lang.String - 数据源中与指定邮件合并字段关联的字段名称。
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
### iterator() {#iterator--}
```
public Iterator iterator()
```


返回一个字典迭代器对象，该对象可用于迭代集合中的所有项目。

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




### remove(String document字段Name) {#remove-java.lang.String-}
```
public void remove(String document字段Name)
```


删除字段映射。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document字段Name | java.lang.String | 文档中邮件合并字段的区分大小写的名称。 |

### set(String document字段Name, String value) {#set-java.lang.String-java.lang.String-}
```
public void set(String document字段Name, String value)
```


设置与指定邮件合并字段关联的数据源中的字段名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document字段Name | java.lang.String |  |
| value | java.lang.String | 与指定邮件合并字段关联的数据源中的字段名称。 |

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
