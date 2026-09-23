---
title: "FootnoteSeparatorCollection"
linktitle: "FootnoteSeparatorCollection"
second_title: "Aspose.Words per Java"
description: "Fornisce accesso tipizzato ai nodi TAspose.Words.Notes.FootnoteSeparator di un documento in Java."
type: docs
weight: 344
url: /it/java/com.aspose.words/footnoteseparatorcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class FootnoteSeparatorCollection implements Cloneable, Iterable
```

Fornisce accesso tipizzato ai nodi **T:Aspose.Words.Notes.FootnoteSeparator** di un documento.

 **Examples:** 

Mostra come gestire il formato del separatore di nota a piè di pagina.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator footnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.FOOTNOTE_SEPARATOR);
 // Align footnote separator.
 footnoteSeparator.getFirstParagraph().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 
```
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getByFootnoteSeparatorType(int separatorType)](#getByFootnoteSeparatorType-int) |  |
| [iterator()](#iterator) |  |
### getByFootnoteSeparatorType(int separatorType) {#getByFootnoteSeparatorType-int}
```
public FootnoteSeparator getByFootnoteSeparatorType(int separatorType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
