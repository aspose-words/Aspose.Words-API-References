---
title: "FootnoteSeparatorCollection"
linktitle: "FootnoteSeparatorCollection"
second_title: "Aspose.Words Java için"
description: "Java'da bir belgenin TAspose.Words.Notes.FootnoteSeparator düğümlerine tipli erişim sağlar."
type: docs
weight: 344
url: /tr/java/com.aspose.words/footnoteseparatorcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class FootnoteSeparatorCollection implements Cloneable, Iterable
```

Bir belgenin **T:Aspose.Words.Notes.FootnoteSeparator** düğümlerine tipli erişim sağlar.

 **Examples:** 

Dipnot ayırıcı biçimini nasıl yöneteceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator footnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.FOOTNOTE_SEPARATOR);
 // Align footnote separator.
 footnoteSeparator.getFirstParagraph().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 
```
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getByFootnoteSeparatorType(int separatorType)](#getByFootnoteSeparatorType-int) |  |
| [iterator()](#iterator) |  |
### getByFootnoteSeparatorType(int separatorType) {#getByFootnoteSeparatorType-int}
```
public FootnoteSeparator getByFootnoteSeparatorType(int separatorType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
