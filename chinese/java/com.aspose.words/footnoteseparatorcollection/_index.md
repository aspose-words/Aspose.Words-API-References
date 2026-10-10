---
title: "FootnoteSeparatorCollection"
linktitle: "FootnoteSeparatorCollection"
second_title: "Aspose.Words for Java"
description: "在 Java 中提供对文档中 TAspose.Words.Notes.FootnoteSeparator 节点的类型化访问。"
type: docs
weight: 344
url: /zh/java/com.aspose.words/footnoteseparatorcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class FootnoteSeparatorCollection implements Cloneable, Iterable
```

提供对文档中 **T:Aspose.Words.Notes.FootnoteSeparator** 节点的类型化访问。

 **Examples:** 

展示如何管理脚注分隔符格式。

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator footnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.FOOTNOTE_SEPARATOR);
 // Align footnote separator.
 footnoteSeparator.getFirstParagraph().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 
```
## 方法

| 方法 | 描述 |
| --- | --- |
| [getByFootnoteSeparatorType(int separatorType)](#getByFootnoteSeparatorType-int) |  |
| [iterator()](#iterator) |  |
### getByFootnoteSeparatorType(int separatorType) {#getByFootnoteSeparatorType-int}
```
public FootnoteSeparator getByFootnoteSeparatorType(int separatorType)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| separatorType | int |  |

**Returns:**
[FootnoteSeparator](../../com.aspose.words/footnoteseparator/)
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
