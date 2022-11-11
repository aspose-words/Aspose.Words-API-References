---
title: FontInfoCollection
second_title: Aspose.Words for Java API Reference
description: 表示文档中使用的字体集合。
type: docs
weight: 281
url: /zh/java/com.aspose.words/fontinfocollection/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Iterable
```
public class FontInfoCollection implements Iterable
```

表示文档中使用的字体集合。

要了解更多信息，请访问**Working with Fonts**文档文章。

项目是[FontInfo](../../com.aspose.words/fontinfo)对象。

您不直接创建此类的实例。使用[DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--)属性来访问文档中定义的字体集合。
## 方法

| 方法 | 描述 |
| --- | --- |
| [contains(String name)](#contains-java.lang.String-) | 确定集合是否包含具有给定名称的字体。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 获取指定索引处的字体。 |
| [get(String name)](#get-java.lang.String-) | 提供对集合项目的访问。 |
| [get班级()](#get班级--) |  |
| [getCount()](#getCount--) | 获取集合中包含的元素数。 |
| [getEmbedSystemFonts()](#getEmbedSystemFonts--) | 指定是否将系统字体嵌入到文档中。 |
| [getEmbedTrue类型Fonts()](#getEmbedTrue类型Fonts--) | 指定保存时是否在文档中嵌入 True类型 字体。 |
| [getSaveSubsetFonts()](#getSaveSubsetFonts--) | 指定是否将嵌入的 True类型 字体的子集与文档一起保存。 |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | 返回一个迭代器对象，该对象可用于迭代集合中的所有项目。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setEmbedSystemFonts(boolean value)](#setEmbedSystemFonts-boolean-) | 指定是否将系统字体嵌入到文档中。 |
| [setEmbedTrue类型Fonts(boolean value)](#setEmbedTrue类型Fonts-boolean-) | 指定保存时是否在文档中嵌入 True类型 字体。 |
| [setSaveSubsetFonts(boolean value)](#setSaveSubsetFonts-boolean-) | 指定是否将嵌入的 True类型 字体的子集与文档一起保存。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


确定集合是否包含具有给定名称的字体。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 要查找的字体的不区分大小写的名称。 |

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
public FontInfo get(int index)
```


获取指定索引处的字体。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 字体的从零开始的索引。 |

**退货:**
[FontInfo](../../com.aspose.words/fontinfo) - 指定索引处的字体。
### get(String name) {#get-java.lang.String-}
```
public FontInfo get(String name)
```


提供对集合项目的访问。获取具有指定名称的字体。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 要查找的字体的不区分大小写的名称。 |

**退货:**
[FontInfo](../../com.aspose.words/fontinfo) - 相应的[FontInfo](../../com.aspose.words/fontinfo)价值。
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
### getEmbedSystemFonts() {#getEmbedSystemFonts--}
```
public boolean getEmbedSystemFonts()
```


指定是否将系统字体嵌入到文档中。此属性的默认值为**false**.

此选项仅在以下情况下有效[getEmbedTrue类型Fonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrue类型Fonts--) / [setEmbedTrue类型Fonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrue类型Fonts-boolean-)选项设置为**true**.

如果用户在东亚系统上并且想要创建一个可供系统上没有该语言字体的其他人可读的文档，则将此属性设置为 True 很有用。例如，日文系统上的用户可以选择将字体嵌入文档中，以便日文文档在所有系统上都可以阅读。

此选项仅适用于 DOC、DOCX 和 RTF 格式。

**退货:**
boolean - 对应的布尔值。
### getEmbedTrue类型Fonts() {#getEmbedTrue类型Fonts--}
```
public boolean getEmbedTrue类型Fonts()
```


指定保存时是否在文档中嵌入 True类型 字体。此属性的默认值为**false**.

嵌入 True类型 字体允许其他人使用创建它时使用的相同字体查看文档，但可能会大大增加文档大小。

此选项仅适用于 DOC、DOCX 和 RTF 格式。

**退货:**
boolean - 对应的布尔值。
### getSaveSubsetFonts() {#getSaveSubsetFonts--}
```
public boolean getSaveSubsetFonts()
```


指定是否将嵌入的 True类型 字体的子集与文档一起保存。此属性的默认值为**false**.

此选项仅在以下情况下有效[getEmbedTrue类型Fonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrue类型Fonts--) / [setEmbedTrue类型Fonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrue类型Fonts-boolean-)属性设置为**true**.

此选项仅适用于 DOC、DOCX 和 RTF 格式。

**退货:**
boolean - 对应的布尔值。
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




### setEmbedSystemFonts(boolean value) {#setEmbedSystemFonts-boolean-}
```
public void setEmbedSystemFonts(boolean value)
```


指定是否将系统字体嵌入到文档中。此属性的默认值为**false**.

此选项仅在以下情况下有效[getEmbedTrue类型Fonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrue类型Fonts--) / [setEmbedTrue类型Fonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrue类型Fonts-boolean-)选项设置为**true**.

如果用户在东亚系统上并且想要创建一个可供系统上没有该语言字体的其他人可读的文档，则将此属性设置为 True 很有用。例如，日文系统上的用户可以选择将字体嵌入文档中，以便日文文档在所有系统上都可以阅读。

此选项仅适用于 DOC、DOCX 和 RTF 格式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setEmbedTrue类型Fonts(boolean value) {#setEmbedTrue类型Fonts-boolean-}
```
public void setEmbedTrue类型Fonts(boolean value)
```


指定保存时是否在文档中嵌入 True类型 字体。此属性的默认值为**false**.

嵌入 True类型 字体允许其他人使用创建它时使用的相同字体查看文档，但可能会大大增加文档大小。

此选项仅适用于 DOC、DOCX 和 RTF 格式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSaveSubsetFonts(boolean value) {#setSaveSubsetFonts-boolean-}
```
public void setSaveSubsetFonts(boolean value)
```


指定是否将嵌入的 True类型 字体的子集与文档一起保存。此属性的默认值为**false**.

此选项仅在以下情况下有效[getEmbedTrue类型Fonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrue类型Fonts--) / [setEmbedTrue类型Fonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrue类型Fonts-boolean-)属性设置为**true**.

此选项仅适用于 DOC、DOCX 和 RTF 格式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

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
