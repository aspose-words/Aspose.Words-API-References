---
title: "EndnotePosition"
linktitle: "EndnotePosition"
second_title: "Aspose.Words Java için"
description: "Java'da dipnot konumunu tanımlar."
type: docs
weight: 190
url: /tr/java/com.aspose.words/endnoteposition/
---

**Inheritance:**
java.lang.Object
```
public class EndnotePosition
```

Dipnot konumunu tanımlar.

 **Examples:** 

Belgenin dipnotları topladığı ve gösterdiği farklı bir yeri nasıl seçeceğinizi gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [END_OF_DOCUMENT](#END-OF-DOCUMENT) | Dipnotlar belgenin sonunda çıktılanır. |
| [END_OF_SECTION](#END-OF-SECTION) | Dipnotlar bölümün sonunda çıktılanır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String endnotePositionName)](#fromName-java.lang.String) |  |
| [getName(int endnotePosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int endnotePosition)](#toString-int) |  |
### END_OF_DOCUMENT {#END-OF-DOCUMENT}
```
public static int END_OF_DOCUMENT
```


Dipnotlar belgenin sonunda çıktılanır.

### END_OF_SECTION {#END-OF-SECTION}
```
public static int END_OF_SECTION
```


Dipnotlar bölümün sonunda çıktılanır.

### length {#length}
```
public static int length
```


### fromName(String endnotePositionName) {#fromName-java.lang.String}
```
public static int fromName(String endnotePositionName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| endnotePositionName | java.lang.String |  |

**Returns:**
int
### getName(int endnotePosition) {#getName-int}
```
public static String getName(int endnotePosition)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| endnotePosition | int |  |

**Returns:**
java.lang.String
