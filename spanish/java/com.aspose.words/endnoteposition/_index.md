---
title: "EndnotePosition"
linktitle: "EndnotePosition"
second_title: "Aspose.Words para Java"
description: "Define la posición de la nota al final en Java."
type: docs
weight: 190
url: /es/java/com.aspose.words/endnoteposition/
---

**Inheritance:**
java.lang.Object
```
public class EndnotePosition
```

Define la posición de la nota al final.

 **Examples:** 

Muestra cómo seleccionar un lugar diferente donde el documento recopila y muestra sus notas al final.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // An endnote is a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting an endnote adds a small superscript reference symbol
 // at the main body text where we insert the endnote.
 // Each endnote also creates an entry at the end of the document, consisting of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertEndnote" method.
 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote contents.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("This is the second section.");

 // We can use the "Position" property to determine where the document will place all its endnotes.
 // If we set the value of the "Position" property to "EndnotePosition.EndOfDocument",
 // every footnote will show up in a collection at the end of the document. This is the default value.
 // If we set the value of the "Position" property to "EndnotePosition.EndOfSection",
 // every footnote will show up in a collection at the end of the section whose text contains the endnote's reference mark.
 doc.getEndnoteOptions().setPosition(endnotePosition);

 doc.save(getArtifactsDir() + "InlineStory.PositionEndnote.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [END_OF_DOCUMENT](#END-OF-DOCUMENT) | Las notas al final se generan al final del documento. |
| [END_OF_SECTION](#END-OF-SECTION) | Las notas al final se generan al final de la sección. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String endnotePositionName)](#fromName-java.lang.String) |  |
| [getName(int endnotePosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int endnotePosition)](#toString-int) |  |
### END_OF_DOCUMENT {#END-OF-DOCUMENT}
```
public static int END_OF_DOCUMENT
```


Las notas al final se generan al final del documento.

### END_OF_SECTION {#END-OF-SECTION}
```
public static int END_OF_SECTION
```


Las notas al final se generan al final de la sección.

### length {#length}
```
public static int length
```


### fromName(String endnotePositionName) {#fromName-java.lang.String}
```
public static int fromName(String endnotePositionName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| endnotePositionName | java.lang.String |  |

**Returns:**
int
### getName(int endnotePosition) {#getName-int}
```
public static String getName(int endnotePosition)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| endnotePosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int endnotePosition) {#toString-int}
```
public static String toString(int endnotePosition)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| endnotePosition | int |  |

**Returns:**
java.lang.String
