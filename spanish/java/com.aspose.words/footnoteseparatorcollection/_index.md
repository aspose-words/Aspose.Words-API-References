---
title: "FootnoteSeparatorCollection"
linktitle: "FootnoteSeparatorCollection"
second_title: "Aspose.Words para Java"
description: "Proporciona acceso tipado a los nodos TAspose.Words.Notes.FootnoteSeparator de un documento en Java."
type: docs
weight: 344
url: /es/java/com.aspose.words/footnoteseparatorcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class FootnoteSeparatorCollection implements Cloneable, Iterable
```

Proporciona acceso tipado a los nodos **T:Aspose.Words.Notes.FootnoteSeparator** de un documento.

 **Examples:** 

Muestra cómo gestionar el formato del separador de notas al pie.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator footnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.FOOTNOTE_SEPARATOR);
 // Align footnote separator.
 footnoteSeparator.getFirstParagraph().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 
```
## Métodos

| Método | Descripción |
| --- | --- |
| [getByFootnoteSeparatorType(int separatorType)](#getByFootnoteSeparatorType-int) |  |
| [iterator()](#iterator) |  |
### getByFootnoteSeparatorType(int separatorType) {#getByFootnoteSeparatorType-int}
```
public FootnoteSeparator getByFootnoteSeparatorType(int separatorType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
