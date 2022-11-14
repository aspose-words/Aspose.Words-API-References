---
title: HtmlInsertOptions
second_title: Aspose.Words for Java API 参考
description: 指定 MAspose.Words.DocumentBuilder.InsertHtmlSystem.StringAspose.Words.HtmlInsertOptions 方法的选项。
type: docs
weight: 327
url: /zh/java/com.aspose.words/htmlinsertoptions/
---

**遗产:**
java.lang.Object
```
public class HtmlInsertOptions
```

指定选项**M:Aspose.Words.DocumentBuilder.InsertHtml(System.String,Aspose.Words.HtmlInsertOptions)**方法。
## 字段

| 场地 | 描述 |
| --- | --- |
| [NONE](#NONE) | 插入 HTML 时使用默认选项。 |
| [PRESERVE_BLOCKS](#PRESERVE-BLOCKS) | 保留块级元素的属性。 |
| [REMOVE_LAST_EMPTY_PARAGRAPH](#REMOVE-LAST-EMPTY-PARAGRAPH) | 删除通常插入到以块级元素结尾的 HTML 之后的空段落。 |
| [USE_BUILDER_FORMATTING](#USE-BUILDER-FORMATTING) | 使用中指定的字体和段落格式[DocumentBuilder](../../com.aspose.words/documentbuilder)作为从 HTML 插入的文本的基本格式。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String htmlInsertOptionsName)](#fromName-java.lang.String-) |  |
| [fromNames(Set htmlInsertOptionsNames)](#fromNames-java.util.Set-) |  |
| [getClass()](#getClass--) |  |
| [getName(int htmlInsertOptions)](#getName-int-) |  |
| [getNames(int htmlInsertOptions)](#getNames-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int htmlInsertOptions)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### NONE {#NONE}
```
public static int NONE
```


插入 HTML 时使用默认选项。

### PRESERVE_BLOCKS {#PRESERVE-BLOCKS}
```
public static int PRESERVE_BLOCKS
```


保留块级元素的属性。

默认情况下，父块的属性被合并并存储在其子元素（即段落或表格）中。如果指定此选项，则每个块的属性将单独存储在特殊的逻辑结构中。因此，此选项可以更好地保留 HTML 文档中的各个边框和边距，并获得更好的转换结果。缺点是生成的文档更难修改，因为存储在逻辑结构中的边框和边距不可用于编辑。

仅保留“body”、“div”和“blockquote”HTML 元素的边距和边框。每个 HTML 元素的属性都是单独存储的。

如果指定了此选项，Aspose.Words 会模仿 MS Word 的有关导入块属性的行为。

### REMOVE_LAST_EMPTY_PARAGRAPH {#REMOVE-LAST-EMPTY-PARAGRAPH}
```
public static int REMOVE_LAST_EMPTY_PARAGRAPH
```


删除通常插入到以块级元素结尾的 HTML 之后的空段落。默认，[DocumentBuilder](../../com.aspose.words/documentbuilder)确保从 HTML 导入的最后一个块级元素在导入后关闭，并在元素后插入一个分节符。此段落分隔符将从 HTML 导入的内容与模板文档的内容分开。但是，如果将 HTML 片段插入到空段落中，则该段落分隔符将创建一个额外的空段落。如果不希望出现这种行为，请指定此选项。

### USE_BUILDER_FORMATTING {#USE-BUILDER-FORMATTING}
```
public static int USE_BUILDER_FORMATTING
```


使用中指定的字体和段落格式[DocumentBuilder](../../com.aspose.words/documentbuilder)作为从 HTML 插入的文本的基本格式。

如果未指定此选项，则格式化[DocumentBuilder](../../com.aspose.words/documentbuilder)被忽略并使用默认 HTML 格式插入文本。因此，文本看起来就像在浏览器中呈现的一样。

如果指定了此选项，则插入文本的格式将基于中指定的格式[DocumentBuilder](../../com.aspose.words/documentbuilder)，并且文本看起来好像是使用[DocumentBuilder.write(java.lang.String)](../../com.aspose.words/documentbuilder\#write-java.lang.String-).

### length {#length}
```
public static int length
```


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
### fromName(String htmlInsertOptionsName) {#fromName-java.lang.String-}
```
public static int fromName(String htmlInsertOptionsName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| htmlInsertOptionsName | java.lang.String |  |

**退货:**
整数
### fromNames(Set htmlInsertOptionsNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set htmlInsertOptionsNames)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| htmlInsertOptionsNames | java.util.Set |  |

**退货:**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getName(int htmlInsertOptions) {#getName-int-}
```
public static String getName(int htmlInsertOptions)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**退货:**
java.lang.String
### getNames(int htmlInsertOptions) {#getNames-int-}
```
public static Set getNames(int htmlInsertOptions)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**退货:**
java.util.Set
### getValues() {#getValues--}
```
public static int[] getValues()
```




**退货:**
整数[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
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
### toString(int htmlInsertOptions) {#toString-int-}
```
public static String toString(int htmlInsertOptions)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**退货:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int-}
```
public static String toStringSet(int attr)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| attr | int |  |

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
