---
title: "MarkupLevel"
linktitle: "MarkupLevel"
second_title: "Aspose.Words für Java"
description: "Gibt die Ebene im Dokumentbaum an, in der ein bestimmtes StructuredDocumentTag in Java auftreten kann."
type: docs
weight: 458
url: /de/java/com.aspose.words/markuplevel/
---

**Inheritance:**
java.lang.Object
```
public class MarkupLevel
```

Gibt die Ebene im Dokumentbaum an, in der ein bestimmtes [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) auftreten kann.

 **Examples:** 

Zeigt, wie man mit Stilen für Inhaltssteuerelemente arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways to apply a style from the document to a structured document tag.
 // 1 -  Apply a style object from the document's style collection:
 Style quoteStyle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.QUOTE);
 StructuredDocumentTag sdtPlainText = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);
 sdtPlainText.setStyle(quoteStyle);

 // 2 -  Reference a style in the document by name:
 StructuredDocumentTag sdtRichText = new StructuredDocumentTag(doc, SdtType.RICH_TEXT, MarkupLevel.INLINE);
 sdtRichText.setStyleName("Quote");

 builder.insertNode(sdtPlainText);
 builder.insertNode(sdtRichText);

 Assert.assertEquals(NodeType.STRUCTURED_DOCUMENT_TAG, sdtPlainText.getNodeType());

 NodeCollection tags = doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG, true);

 for (StructuredDocumentTag sdt : (Iterable) tags) {
     Assert.assertEquals(StyleIdentifier.QUOTE, sdt.getStyle().getStyleIdentifier());
     Assert.assertEquals("Quote", sdt.getStyleName());
 }
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BLOCK](#BLOCK) | Das Element tritt auf Blockebene auf (z. B. |
| [CELL](#CELL) | Das Element tritt zwischen Zellen in einer Zeile auf. |
| [INLINE](#INLINE) | Das Element tritt auf Inlineebene auf (z. B. |
| [ROW](#ROW) | Das Element tritt zwischen Zeilen in einer Tabelle auf. |
| [UNKNOWN](#UNKNOWN) | Gibt den unbekannten oder ungültigen Wert an. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String markupLevelName)](#fromName-java.lang.String) |  |
| [getName(int markupLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markupLevel)](#toString-int) |  |
### BLOCK {#BLOCK}
```
public static int BLOCK
```


Das Element tritt auf Blockebene auf (z. B. zwischen Tabellen und Absätzen).

### CELL {#CELL}
```
public static int CELL
```


Das Element tritt zwischen Zellen in einer Zeile auf.

### INLINE {#INLINE}
```
public static int INLINE
```


Das Element tritt auf Inlineebene auf (z. B. zwischen Textläufen).

### ROW {#ROW}
```
public static int ROW
```


Das Element tritt zwischen Zeilen in einer Tabelle auf.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Gibt den unbekannten oder ungültigen Wert an.

### length {#length}
```
public static int length
```


### fromName(String markupLevelName) {#fromName-java.lang.String}
```
public static int fromName(String markupLevelName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| markupLevelName | java.lang.String |  |

**Returns:**
int
### getName(int markupLevel) {#getName-int}
```
public static String getName(int markupLevel)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| markupLevel | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int markupLevel) {#toString-int}
```
public static String toString(int markupLevel)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| markupLevel | int |  |

**Returns:**
java.lang.String
