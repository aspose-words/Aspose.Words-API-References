---
title: MarkupLevel
linktitle: MarkupLevel
second_title: Aspose.Words for Java
description: Specifies the level in the document tree where a particular StructuredDocumentTag can occur in Java.
type: docs
weight: 418
url: /java/com.aspose.words/markuplevel/
---

**Inheritance:**
java.lang.Object
```
public class MarkupLevel
```

Specifies the level in the document tree where a particular [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) can occur.

 **Examples:** 

Shows how to work with styles for content control elements.

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
## Fields

| Field | Description |
| --- | --- |
| [BLOCK](#BLOCK) | The element occurs at the block level (e.g. |
| [CELL](#CELL) | The element occurs among cells in a row. |
| [INLINE](#INLINE) | The element occurs at the inline level (e.g. |
| [ROW](#ROW) | The element occurs among rows in a table. |
| [UNKNOWN](#UNKNOWN) | Specifies the unknown or invalid value. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String markupLevelName)](#fromName-java.lang.String) |  |
| [getName(int markupLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markupLevel)](#toString-int) |  |
### BLOCK {#BLOCK}
```
public static int BLOCK
```


The element occurs at the block level (e.g. among tables and paragraphs).

### CELL {#CELL}
```
public static int CELL
```


The element occurs among cells in a row.

### INLINE {#INLINE}
```
public static int INLINE
```


The element occurs at the inline level (e.g. among as runs of text).

### ROW {#ROW}
```
public static int ROW
```


The element occurs among rows in a table.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Specifies the unknown or invalid value.

### length {#length}
```
public static int length
```


### fromName(String markupLevelName) {#fromName-java.lang.String}
```
public static int fromName(String markupLevelName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| markupLevelName | java.lang.String |  |

**Returns:**
int
### getName(int markupLevel) {#getName-int}
```
public static String getName(int markupLevel)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| markupLevel | int |  |

**Returns:**
java.lang.String
