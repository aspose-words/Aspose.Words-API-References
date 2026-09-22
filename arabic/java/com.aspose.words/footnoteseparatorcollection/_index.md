---
title: "FootnoteSeparatorCollection"
linktitle: "FootnoteSeparatorCollection"
second_title: "Aspose.Words لـ Java"
description: "يوفر وصولًا مكتوبًا إلى عقد TAspose.Words.Notes.FootnoteSeparator في مستند بلغة Java."
type: docs
weight: 344
url: /ar/java/com.aspose.words/footnoteseparatorcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class FootnoteSeparatorCollection implements Cloneable, Iterable
```

يوفر وصولًا مكتوبًا إلى عقد **T:Aspose.Words.Notes.FootnoteSeparator** في المستند.

 **Examples:** 

يوضح كيفية إدارة تنسيق فاصل الحاشية.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator footnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.FOOTNOTE_SEPARATOR);
 // Align footnote separator.
 footnoteSeparator.getFirstParagraph().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 
```
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getByFootnoteSeparatorType(int separatorType)](#getByFootnoteSeparatorType-int) |  |
| [iterator()](#iterator) |  |
### getByFootnoteSeparatorType(int separatorType) {#getByFootnoteSeparatorType-int}
```
public FootnoteSeparator getByFootnoteSeparatorType(int separatorType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
