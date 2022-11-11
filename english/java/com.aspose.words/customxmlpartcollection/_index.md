---
title: CustomXmlPartCollection
second_title: Aspose.Words for Java API 参考
description: 表示自定义 XML 部件的集合。
type: docs
weight: 105
url: /zh/java/com.aspose.words/customxmlpartcollection/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Iterable
```
public class CustomXmlPartCollection implements Iterable
```

表示自定义 XML 部件的集合。项目是[CustomXmlPart](../../com.aspose.words/customxmlpart)对象。

要了解更多信息，请访问**Structured Document Tags or Content Control**文档文章。

您通常不需要创建此类的实例。您可以通过以下方式访问存储在文档中的自定义 XML 数据[Document.getCustomXmlParts()](../../com.aspose.words/document\#getCustomXmlParts--) / [Document.setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-)财产。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [add(CustomXmlPart part)](#add-com.aspose.words.CustomXmlPart-) | 将项目添加到集合中。 |
| [add(String id, String xml)](#add-java.lang.String-java.lang.String-) | 使用指定的 XML 创建一个新的 XML 部件并将其添加到集合中。 |
| [clear()](#clear--) | 从集合中移除所有元素。 |
| [deepClone()](#deepClone--) | 制作此集合及其项目的深层副本。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 获取指定索引处的项目。 |
| [getById(String id)](#getById-java.lang.String-) | 按标识符查找并返回自定义 XML 部件。 |
| [get班级()](#get班级--) |  |
| [getCount()](#getCount--) | 获取集合中包含的元素数。 |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | 返回一个迭代器对象，该对象可用于迭代集合中的所有项目。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeAt(int index)](#removeAt-int-) | 删除指定索引处的项目。 |
| [set(int index, CustomXmlPart value)](#set-int-com.aspose.words.CustomXmlPart-) | 在指定索引处设置项目。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(CustomXmlPart part) {#add-com.aspose.words.CustomXmlPart-}
```
public void add(CustomXmlPart part)
```


将项目添加到集合中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| part | [CustomXmlPart](../../com.aspose.words/customxmlpart) | 要添加的自定义 XML 部分。 |

### add(String id, String xml) {#add-java.lang.String-java.lang.String-}
```
public CustomXmlPart add(String id, String xml)
```


使用指定的 XML 创建一个新的 XML 部件并将其添加到集合中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| id | java.lang.String | 新的自定义 XML 部件的标识符。 |
| xml | java.lang.String | 零件的 XML 数据。 |

**退货:**
[CustomXmlPart](../../com.aspose.words/customxmlpart) - 创建自定义 XML 部分。
### clear() {#clear--}
```
public void clear()
```


从集合中移除所有元素。

### deepClone() {#deepClone--}
```
public CustomXmlPartCollection deepClone()
```


制作此集合及其项目的深层副本。

**退货:**
[CustomXmlPartCollection](../../com.aspose.words/customxmlpartcollection)
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
public CustomXmlPart get(int index)
```


获取指定索引处的项目。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 项目的从零开始的索引。 |

**退货:**
[CustomXmlPart](../../com.aspose.words/customxmlpart) - 指定索引处的项目。
### getById(String id) {#getById-java.lang.String-}
```
public CustomXmlPart getById(String id)
```


按标识符查找并返回自定义 XML 部件。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| id | java.lang.String | 标识自定义 XML 部分的区分大小写的字符串。 |

**退货:**
[CustomXmlPart](../../com.aspose.words/customxmlpart) - 如果未找到具有指定标识符的自定义 XML 部分，则返回 null。
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




### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


删除指定索引处的项目。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 从零开始的索引。 |

### set(int index, CustomXmlPart value) {#set-int-com.aspose.words.CustomXmlPart-}
```
public void set(int index, CustomXmlPart value)
```


在指定索引处设置项目。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 项目的从零开始的索引。 |
| value | [CustomXmlPart](../../com.aspose.words/customxmlpart) | 指定索引处的项目。 |

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
