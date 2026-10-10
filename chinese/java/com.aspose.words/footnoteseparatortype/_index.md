---
title: "FootnoteSeparatorType"
linktitle: "FootnoteSeparatorType"
second_title: "Aspose.Words for Java"
description: "指定 Java 中脚注/尾注分隔符的类型。"
type: docs
weight: 345
url: /zh/java/com.aspose.words/footnoteseparatortype/
---

**Inheritance:**
java.lang.Object
```
public class FootnoteSeparatorType
```

指定脚注/尾注分隔符的类型。

 **Examples:** 

展示如何移除尾注分隔符。

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator endnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.ENDNOTE_SEPARATOR);
 // Remove endnote separator.
 endnoteSeparator.getFirstParagraph().getFirstChild().remove();
 
```

展示如何管理脚注分隔符格式。

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator footnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.FOOTNOTE_SEPARATOR);
 // Align footnote separator.
 footnoteSeparator.getFirstParagraph().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [ENDNOTE_CONTINUATION_NOTICE](#ENDNOTE-CONTINUATION-NOTICE) | 当尾注文本需在下一页继续时，打印在页面尾注文本下方。 |
| [ENDNOTE_CONTINUATION_SEPARATOR](#ENDNOTE-CONTINUATION-SEPARATOR) | 当文本需从前一页继续时，打印在页面尾注文本上方。 |
| [ENDNOTE_SEPARATOR](#ENDNOTE-SEPARATOR) | 正文与尾注文本之间的分隔符。 |
| [FOOTNOTE_CONTINUATION_NOTICE](#FOOTNOTE-CONTINUATION-NOTICE) | 当脚注文本需在下一页继续时，打印在页面脚注文本下方。 |
| [FOOTNOTE_CONTINUATION_SEPARATOR](#FOOTNOTE-CONTINUATION-SEPARATOR) | 当文本需从前一页继续时，打印在页面脚注文本上方。 |
| [FOOTNOTE_SEPARATOR](#FOOTNOTE-SEPARATOR) | 正文与脚注文本之间的分隔符。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String footnoteSeparatorTypeName)](#fromName-java.lang.String) |  |
| [getName(int footnoteSeparatorType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int footnoteSeparatorType)](#toString-int) |  |
### ENDNOTE_CONTINUATION_NOTICE {#ENDNOTE-CONTINUATION-NOTICE}
```
public static int ENDNOTE_CONTINUATION_NOTICE
```


当尾注文本需在下一页继续时，打印在页面尾注文本下方。

### ENDNOTE_CONTINUATION_SEPARATOR {#ENDNOTE-CONTINUATION-SEPARATOR}
```
public static int ENDNOTE_CONTINUATION_SEPARATOR
```


当文本需从前一页继续时，打印在页面尾注文本上方。

### ENDNOTE_SEPARATOR {#ENDNOTE-SEPARATOR}
```
public static int ENDNOTE_SEPARATOR
```


正文与尾注文本之间的分隔符。

### FOOTNOTE_CONTINUATION_NOTICE {#FOOTNOTE-CONTINUATION-NOTICE}
```
public static int FOOTNOTE_CONTINUATION_NOTICE
```


当脚注文本需在下一页继续时，打印在页面脚注文本下方。

### FOOTNOTE_CONTINUATION_SEPARATOR {#FOOTNOTE-CONTINUATION-SEPARATOR}
```
public static int FOOTNOTE_CONTINUATION_SEPARATOR
```


当文本需从前一页继续时，打印在页面脚注文本上方。

### FOOTNOTE_SEPARATOR {#FOOTNOTE-SEPARATOR}
```
public static int FOOTNOTE_SEPARATOR
```


正文与脚注文本之间的分隔符。

### length {#length}
```
public static int length
```


### fromName(String footnoteSeparatorTypeName) {#fromName-java.lang.String}
```
public static int fromName(String footnoteSeparatorTypeName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| footnoteSeparatorTypeName | java.lang.String |  |

**Returns:**
int
### getName(int footnoteSeparatorType) {#getName-int}
```
public static String getName(int footnoteSeparatorType)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| footnoteSeparatorType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int footnoteSeparatorType) {#toString-int}
```
public static String toString(int footnoteSeparatorType)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| footnoteSeparatorType | int |  |

**Returns:**
java.lang.String
