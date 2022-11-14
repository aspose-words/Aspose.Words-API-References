---
title: CustomDocumentProperties
second_title: Aspose.Words for Java API 参考
description: 自定义文档属性的集合。
type: docs
weight: 101
url: /zh/java/com.aspose.words/customdocumentproperties/
---

**遗产:**
java.lang.Object, [com.aspose.words.DocumentPropertyCollection](../../com.aspose.words/documentpropertycollection)
```
public class CustomDocumentProperties extends DocumentPropertyCollection
```

自定义文档属性的集合。

要了解更多信息，请访问**Work with Document Properties**文档文章。

每个[DocumentProperty](../../com.aspose.words/documentproperty)object 表示容器文档的自定义属性。

属性的名称不区分大小写。

集合中的属性按名称的字母顺序排序。
## 方法

| 方法 | 描述 |
| --- | --- |
| [add(String name, boolean value)](#add-java.lang.String-boolean-) | 创建一个新的自定义文档属性**PropertyType.Boolean**数据类型。 |
| [add(String name, double value)](#add-java.lang.String-double-) | 创建一个新的自定义文档属性**PropertyType.Float**数据类型。 |
| [add(String name, int value)](#add-java.lang.String-int-) | 创建一个新的自定义文档属性**PropertyType.Number**数据类型。 |
| [add(String name, String value)](#add-java.lang.String-java.lang.String-) | 创建一个新的自定义文档属性。 |
| [add(String name, Date value)](#add-java.lang.String-java.util.Date-) | 创建一个新的自定义文档属性**PropertyType.DateTime**数据类型。 |
| [addLinkToContent(String name, String linkSource)](#addLinkToContent-java.lang.String-java.lang.String-) | 创建一个新的链接到内容自定义文档属性。 |
| [clear()](#clear--) | 从集合中删除所有属性。 |
| [contains(String name)](#contains-java.lang.String-) | 如果集合中存在具有指定名称的属性，则返回 true。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 返回一个[DocumentProperty](../../com.aspose.words/documentproperty)按索引的对象。 |
| [get(String name)](#get-java.lang.String-) | 提供对集合项目的访问。 |
| [getClass()](#getClass--) |  |
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
### add(String name, boolean value) {#add-java.lang.String-boolean-}
```
public DocumentProperty add(String name, boolean value)
```


创建一个新的自定义文档属性**PropertyType.Boolean**数据类型。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 属性的名称。 |
| value | boolean | 财产的价值。 |

**退货:**
[DocumentProperty](../../com.aspose.words/documentproperty) - 新创建的属性对象。
### add(String name, double value) {#add-java.lang.String-double-}
```
public DocumentProperty add(String name, double value)
```


创建一个新的自定义文档属性**PropertyType.Float**数据类型。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 属性的名称。 |
| value | double | 财产的价值。 |

**退货:**
[DocumentProperty](../../com.aspose.words/documentproperty) - 新创建的属性对象。
### add(String name, int value) {#add-java.lang.String-int-}
```
public DocumentProperty add(String name, int value)
```


创建一个新的自定义文档属性**PropertyType.Number**数据类型。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 属性的名称。 |
| value | int | 财产的价值。 |

**退货:**
[DocumentProperty](../../com.aspose.words/documentproperty) - 新创建的属性对象。
### add(String name, String value) {#add-java.lang.String-java.lang.String-}
```
public DocumentProperty add(String name, String value)
```


创建一个新的自定义文档属性。创建一个新的自定义文档属性**PropertyType.String**数据类型。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 属性的名称。 |
| value | java.lang.String | 财产的价值。 |

**退货:**
[DocumentProperty](../../com.aspose.words/documentproperty) - 新创建的属性对象。
### add(String name, Date value) {#add-java.lang.String-java.util.Date-}
```
public DocumentProperty add(String name, Date value)
```


创建一个新的自定义文档属性**PropertyType.DateTime**数据类型。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 属性的名称。 |
| value | java.util.Date | 财产的价值。 |

**退货:**
[DocumentProperty](../../com.aspose.words/documentproperty) - 新创建的属性对象。
### addLinkToContent(String name, String linkSource) {#addLinkToContent-java.lang.String-java.lang.String-}
```
public DocumentProperty addLinkToContent(String name, String linkSource)
```


创建一个新的链接到内容自定义文档属性。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 属性的名称。 |
| linkSource | java.lang.String | 财产的来源。 |

**退货:**
[DocumentProperty](../../com.aspose.words/documentproperty) 新创建的属性对象或链接源无效时为空。
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
| name | java.lang.String | 属性的不区分大小写的名称。 |

**退货:**
boolean - 如果该属性存在于集合中则为真；否则为假。
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

**Note:**在 Java 中，此方法很慢，因为遍历所有节点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 零基指数[DocumentProperty](../../com.aspose.words/documentproperty)检索。 |

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

**Note:**在 Java 中，此方法很慢，因为遍历所有节点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 属性的不区分大小写的名称。 |

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
| name | java.lang.String | 属性的不区分大小写的名称。 |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


删除指定索引处的属性。

**Note:**在 Java 中，此方法很慢，因为遍历所有节点。

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
