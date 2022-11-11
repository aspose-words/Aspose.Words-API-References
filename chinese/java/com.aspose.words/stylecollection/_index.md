---
title: StyleCollection
second_title: Aspose.Words for Java API Reference
description: Style 对象的集合，表示文档中的内置样式和用户定义的样式。
type: docs
weight: 537
url: /zh/java/com.aspose.words/stylecollection/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Cloneable, java.lang.Iterable
```
public class StyleCollection implements Cloneable, Iterable
```

Style 对象的集合，表示文档中的内置样式和用户定义的样式。

要了解更多信息，请访问**Working with Styles and Themes**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [add(int type, String name)](#add-int-java.lang.String-) |  |
| [addCopy(Style style)](#addCopy-com.aspose.words.Style-) | 将样式复制到此集合中。 |
| [clearQuickStyleGallery()](#clearQuickStyleGallery--) | 从“快速样式库”面板中删除所有样式。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 按索引获取样式。 |
| [get(String name)](#get-java.lang.String-) | 从集合中检索样式。 |
| [getByStyleIdentifier(int sti)](#getByStyleIdentifier-int-) |  |
| [get班级()](#get班级--) |  |
| [getCount()](#getCount--) | 获取集合中的样式数。 |
| [getDefaultFont()](#getDefaultFont--) | 获取文档默认文本格式。 |
| [getDefaultParagraphFormat()](#getDefaultParagraphFormat--) | 获取文档默认段落格式。 |
| [getDocument()](#getDocument--) | 获取所有者文档。 |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | 获取一个枚举器对象，该对象将按名称的字母顺序枚举样式。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(int type, String name) {#add-int-java.lang.String-}
```
public Style add(int type, String name)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| type | int |  |
| name | java.lang.String |  |

**退货:**
[Style](../../com.aspose.words/style)
### addCopy(Style style) {#addCopy-com.aspose.words.Style-}
```
public Style addCopy(Style style)
```


将样式复制到此集合中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style) | 要复制的样式。 |

**退货:**
[Style](../../com.aspose.words/style) - 复制样式可供使用。

要复制的样式可以属于同一个文档，也可以属于不同的文档。

链接样式被复制。

此方法不会复制基本样式。

如果集合已经包含同名的样式，则通过添加“自动生成新名称”\_number”后缀，从 0 开始，例如“Normal”\_0", "标题 1\ _1" 等。使用[Style.getName()](../../com.aspose.words/style\#getName--) / [Style.setName(java.lang.String)](../../com.aspose.words/style\#setName-java.lang.String-)setter 用于更改导入样式的名称。
### clearQuickStyleGallery() {#clearQuickStyleGallery--}
```
public void clearQuickStyleGallery()
```


从“快速样式库”面板中删除所有样式。

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
public Style get(int index)
```


按索引获取样式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int |  |

**退货:**
[Style](../../com.aspose.words/style) - 按索引的样式。
### get(String name) {#get-java.lang.String-}
```
public Style get(String name)
```


从集合中检索样式。按名称或别名获取样式。

区分大小写，如果未找到具有给定名称的样式，则返回 null。

如果这是一个尚不存在的内置样式的英文名称，则自动创建它。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String |  |

**退货:**
[Style](../../com.aspose.words/style) - 相应的[Style](../../com.aspose.words/style)价值。
### getByStyleIdentifier(int sti) {#getByStyleIdentifier-int-}
```
public Style getByStyleIdentifier(int sti)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sti | int |  |

**退货:**
[Style](../../com.aspose.words/style)
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


获取集合中的样式数。

**退货:**
int - 集合中的样式数。
### getDefaultFont() {#getDefaultFont--}
```
public Font getDefaultFont()
```


获取文档默认文本格式。

请注意，Microsoft Word 2007 中引入了文档范围的默认值，并且完全支持 OOXML 格式（[LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX)） 只要。早期的文档格式对此功能的支持有限，只能存储字体名称。

**退货:**
[Font](../../com.aspose.words/font) - 文档默认文本格式。
### getDefaultParagraphFormat() {#getDefaultParagraphFormat--}
```
public ParagraphFormat getDefaultParagraphFormat()
```


获取文档默认段落格式。

请注意，Microsoft Word 2007 中引入了文档范围的默认值，并且完全支持 OOXML 格式（[LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX)） 只要。早期的文档格式不支持文档默认段落格式。

**退货:**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - 文档默认段落格式。
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


获取所有者文档。

**退货:**
[DocumentBase](../../com.aspose.words/documentbase) - 所有者文件。
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


获取一个枚举器对象，该对象将按名称的字母顺序枚举样式。

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
