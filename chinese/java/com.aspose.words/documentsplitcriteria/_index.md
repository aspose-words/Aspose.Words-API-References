---
title: DocumentSplitCriteria
second_title: Aspose.Words for Java API 参考
description:指定在保存到或格式化时如何将文档拆分为多个部分。
type: docs
weight: 131
url: /zh/java/com.aspose.words/documentsplitcriteria/
---

**遗产:**
java.lang.Object
```
public class DocumentSplitCriteria
```

指定保存到时如何将文档拆分为多个部分[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB)或者[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3)格式。

[DocumentSplitCriteria](../../com.aspose.words/documentsplitcriteria)是一组可以组合的标志。例如，您可以在同一导出操作中在分页符和标题段落处拆分文档。

不同的标准可以部分重叠。例如，**Heading 1**风格经常被赋予[ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat\#getPageBreakBefore--) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat\#setPageBreakBefore-boolean-)财产，因此它符合两个标准：[PAGE\_BREAK](../../com.aspose.words/documentsplitcriteria\#PAGE-BREAK)和[HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria\#HEADING-PARAGRAPH).某些分节符可能会导致分页符等。在典型情况下，仅指定一个标志是最实用的选项。
## 字段

| 字段 | 描述 |
| --- | --- |
| [COLUMN_BREAK](#COLUMN-BREAK) | 文档在分栏符处分成几部分。 |
| [HEADING_PARAGRAPH](#HEADING-PARAGRAPH) | 文档在使用标题样式格式化的段落中分成几部分**Heading 1**, **Heading 2**等等 |
| [NONE](#NONE) | 文档未拆分。 |
| [PAGE_BREAK](#PAGE-BREAK) | 文档在显式分页符处分成几部分。 |
| [SECTION_BREAK](#SECTION-BREAK) | 文档在任何类型的分节符处拆分为多个部分。 |
| [length](#length) |  |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String documentSplitCriteriaName)](#fromName-java.lang.String-) |  |
| [fromNames(Set documentSplitCriteriaNames)](#fromNames-java.util.Set-) |  |
| [get班级()](#get班级--) |  |
| [getName(int documentSplitCriteria)](#getName-int-) |  |
| [getNames(int documentSplitCriteria)](#getNames-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int documentSplitCriteria)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### COLUMN_BREAK {#COLUMN-BREAK}
```
public static int COLUMN_BREAK
```


文档在分栏符处分成几部分。分栏符可以由[ControlChar.COLUMN\_BREAK](../../com.aspose.words/controlchar\#COLUMN-BREAK)字符或分节符指定新列中新节的开始。

### HEADING_PARAGRAPH {#HEADING-PARAGRAPH}
```
public static int HEADING_PARAGRAPH
```


文档在使用标题样式格式化的段落中分成几部分**Heading 1**, **Heading 2**等一起使用[HtmlSaveOptions.getDocumentSplitHeadingLevel()](../../com.aspose.words/htmlsaveoptions\#getDocumentSplitHeadingLevel--) / [HtmlSaveOptions.setDocumentSplitHeadingLevel(int)](../../com.aspose.words/htmlsaveoptions\#setDocumentSplitHeadingLevel-int-)指定要拆分的标题级别（从 1 到指定级别）。

### NONE {#NONE}
```
public static int NONE
```


文档未拆分。

### PAGE_BREAK {#PAGE-BREAK}
```
public static int PAGE_BREAK
```


文档在显式分页符处分成几部分。分页符可以由[ControlChar.PAGE\_BREAK](../../com.aspose.words/controlchar\#PAGE-BREAK)字符，分节符，指定新页面上新节的开始，或具有其[ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat\#getPageBreakBefore--) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat\#setPageBreakBefore-boolean-)属性设置为 true 。

### SECTION_BREAK {#SECTION-BREAK}
```
public static int SECTION_BREAK
```


文档在任何类型的分节符处拆分为多个部分。

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
### fromName(String documentSplitCriteriaName) {#fromName-java.lang.String-}
```
public static int fromName(String documentSplitCriteriaName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| documentSplitCriteriaName | java.lang.String |  |

**退货:**
整数
### fromNames(Set documentSplitCriteriaNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set documentSplitCriteriaNames)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| documentSplitCriteriaNames | java.util.Set |  |

**退货:**
整数
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getName(int documentSplitCriteria) {#getName-int-}
```
public static String getName(int documentSplitCriteria)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| documentSplitCriteria | int |  |

**退货:**
java.lang.String
### getNames(int documentSplitCriteria) {#getNames-int-}
```
public static Set getNames(int documentSplitCriteria)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| documentSplitCriteria | int |  |

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
### toString(int documentSplitCriteria) {#toString-int-}
```
public static String toString(int documentSplitCriteria)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| documentSplitCriteria | int |  |

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
