---
title: StructuredDocumentTagCollection
second_title: Aspose.Words for Java API 参考
description: 表示指定范围内的结构化文档标签的实例集合。
type: docs
weight: 533
url: /zh/java/com.aspose.words/structureddocumenttagcollection/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Iterable
```
public class StructuredDocumentTagCollection implements Iterable
```

的集合[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag)表示指定范围内的结构化文档标签的实例。

要了解更多信息，请访问**Structured Document Tags or Content Control**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 返回指定索引处的结构化文档标签。 |
| [getById(int id)](#getById-int-) | 按标识符返回结构化文档标签。 |
| [getByTag(String tag)](#getByTag-java.lang.String-) | 返回集合中遇到的第一个带有指定标签的结构化文档标签。 |
| [getByTitle(String title)](#getByTitle-java.lang.String-) | 返回集合中遇到的具有指定标题的第一个结构化文档标记。 |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | 返回集合中结构化文档标签的数量。 |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | 返回一个枚举器对象。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(int id)](#remove-int-) | 删除具有指定标识符的结构化文档标签。 |
| [removeAt(int index)](#removeAt-int-) | 删除指定索引处的结构化文档标记。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
public IStructuredDocumentTag get(int index)
```


返回指定索引处的结构化文档标签。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 集合中的索引。 |

**退货:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag) - 指定索引处的结构化文档标签。
### getById(int id) {#getById-int-}
```
public IStructuredDocumentTag getById(int id)
```


按标识符返回结构化文档标签。

如果找不到具有指定标识符的结构化文档标签，则返回 null。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| id | int | 结构化文档标签标识符。 |

**退货:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag)
### getByTag(String tag) {#getByTag-java.lang.String-}
```
public IStructuredDocumentTag getByTag(String tag)
```


返回集合中遇到的第一个带有指定标签的结构化文档标签。

如果找不到具有指定标签的结构化文档标签，则返回 null。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| tag | java.lang.String | 结构化文档标签的标签。 |

**退货:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag)
### getByTitle(String title) {#getByTitle-java.lang.String-}
```
public IStructuredDocumentTag getByTitle(String title)
```


返回集合中遇到的具有指定标题的第一个结构化文档标记。

如果找不到具有指定标题的结构化文档标签，则返回 null。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| title | java.lang.String | 结构化文档标签的标题。 |

**退货:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag)
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


返回集合中结构化文档标签的数量。

**退货:**
int - 集合中结构化文档标签的数量。
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




### remove(int id) {#remove-int-}
```
public void remove(int id)
```


删除具有指定标识符的结构化文档标签。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| id | int | 结构化文档标签标识符。 |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


删除指定索引处的结构化文档标记。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 集合中的索引。 |

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
