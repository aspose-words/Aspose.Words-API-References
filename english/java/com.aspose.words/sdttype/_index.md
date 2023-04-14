---
title: SdtType
linktitle: SdtType
second_title: Aspose.Words for Java API Reference
description: Specifies the type of a structured document tag SDT node in Java.
type: docs
weight: 517
url: /java/com.aspose.words/sdttype/
---

**Inheritance:**
java.lang.Object
```
public class SdtType
```

Specifies the type of a structured document tag (SDT) node.

 **Examples:** 

Shows how to create group structured document tag at the Row level.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();

 // Create a Group structured document tag at the Row level.
 StructuredDocumentTag groupSdt = new StructuredDocumentTag(doc, SdtType.GROUP, MarkupLevel.ROW);
 table.appendChild(groupSdt);
 groupSdt.isShowingPlaceholderText(false);
 groupSdt.removeAllChildren();

 // Create a child row of the structured document tag.
 Row row = new Row(doc);
 groupSdt.appendChild(row);

 Cell cell = new Cell(doc);
 row.appendChild(cell);

 builder.endTable();

 // Insert cell contents.
 cell.ensureMinimum();
 builder.moveTo(cell.getLastParagraph());
 builder.write("Lorem ipsum dolor.");

 // Insert text after the table.
 builder.moveTo(table.getNextSibling());
 builder.write("Nulla blandit nisi.");

 doc.save(getArtifactsDir() + "StructuredDocumentTag.SdtAtRowLevel.docx");
 
```

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

Shows how to fill a table with data from in an XML part.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 CustomXmlPart xmlPart = doc.getCustomXmlParts().add("Books",
         "" +
                 "" +
                 "Everyday Italian" +
                 "Giada De Laurentiis" +
                 "" +
                 "" +
                 "The C Programming Language" +
                 "Brian W. Kernighan, Dennis M. Ritchie" +
                 "" +
                 "" +
                 "Learning XML" +
                 "Erik T. Ray" +
                 "" +
                 "");

 // Create headers for data from the XML content.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Title");
 builder.insertCell();
 builder.write("Author");
 builder.endRow();
 builder.endTable();

 // Create a table with a repeating section inside.
 StructuredDocumentTag repeatingSectionSdt =
         new StructuredDocumentTag(doc, SdtType.REPEATING_SECTION, MarkupLevel.ROW);
 repeatingSectionSdt.getXmlMapping().setMapping(xmlPart, "/books[1]/book", "");
 table.appendChild(repeatingSectionSdt);

 // Add repeating section item inside the repeating section and mark it as a row.
 // This table will have a row for each element that we can find in the XML document
 // using the "/books[1]/book" XPath, of which there are three.
 StructuredDocumentTag repeatingSectionItemSdt =
         new StructuredDocumentTag(doc, SdtType.REPEATING_SECTION_ITEM, MarkupLevel.ROW);
 repeatingSectionSdt.appendChild(repeatingSectionItemSdt);

 Row row = new Row(doc);
 repeatingSectionItemSdt.appendChild(row);

 // Map XML data with created table cells for the title and author of each book.
 StructuredDocumentTag titleSdt =
         new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.CELL);
 titleSdt.getXmlMapping().setMapping(xmlPart, "/books[1]/book[1]/title[1]", "");
 row.appendChild(titleSdt);

 StructuredDocumentTag authorSdt =
         new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.CELL);
 authorSdt.getXmlMapping().setMapping(xmlPart, "/books[1]/book[1]/author[1]", "");
 row.appendChild(authorSdt);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.RepeatingSectionItem.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [BIBLIOGRAPHY](#BIBLIOGRAPHY) | The SDT represents a bibliography entry. |
| [BUILDING_BLOCK_GALLERY](#BUILDING-BLOCK-GALLERY) | The SDT represents a building block gallery type. |
| [CHECKBOX](#CHECKBOX) | The SDT represents a checkbox when displayed in the document. |
| [CITATION](#CITATION) | The SDT represents a citation. |
| [COMBO_BOX](#COMBO-BOX) | The SDT represents a combo box when displayed in the document. |
| [DATE](#DATE) | The SDT represents a date picker when displayed in the document. |
| [DOC_PART_OBJ](#DOC-PART-OBJ) | The SDT represents a document part type. |
| [DROP_DOWN_LIST](#DROP-DOWN-LIST) | The SDT represents a drop down list when displayed in the document. |
| [ENTITY_PICKER](#ENTITY-PICKER) | The SDT represents an entity picker that allows the user to select an instance of an external content type. |
| [EQUATION](#EQUATION) | The SDT represents an equation. |
| [GROUP](#GROUP) | The SDT represents a restricted grouping when displayed in the document. |
| [NONE](#NONE) | No type is assigned to the SDT. |
| [PICTURE](#PICTURE) | The SDT represents a picture when displayed in the document. |
| [PLAIN_TEXT](#PLAIN-TEXT) | The SDT represents a plain text box when displayed in the document. |
| [REPEATING_SECTION](#REPEATING-SECTION) | The SDT represents repeating section type when displayed in the document. |
| [REPEATING_SECTION_ITEM](#REPEATING-SECTION-ITEM) | The SDT represents repeating section item. |
| [RICH_TEXT](#RICH-TEXT) | The SDT represents a rich text box when displayed in the document. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String sdtTypeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int sdtType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int sdtType)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### BIBLIOGRAPHY {#BIBLIOGRAPHY}
```
public static int BIBLIOGRAPHY
```


The SDT represents a bibliography entry.

### BUILDING_BLOCK_GALLERY {#BUILDING-BLOCK-GALLERY}
```
public static int BUILDING_BLOCK_GALLERY
```


The SDT represents a building block gallery type.

### CHECKBOX {#CHECKBOX}
```
public static int CHECKBOX
```


The SDT represents a checkbox when displayed in the document.

 **Remarks:** 

This is MS-specific feature available since Office 2010 and not supported by the ISO/IEC 29500 OOXML standard.

### CITATION {#CITATION}
```
public static int CITATION
```


The SDT represents a citation.

### COMBO_BOX {#COMBO-BOX}
```
public static int COMBO_BOX
```


The SDT represents a combo box when displayed in the document.

### DATE {#DATE}
```
public static int DATE
```


The SDT represents a date picker when displayed in the document.

### DOC_PART_OBJ {#DOC-PART-OBJ}
```
public static int DOC_PART_OBJ
```


The SDT represents a document part type.

### DROP_DOWN_LIST {#DROP-DOWN-LIST}
```
public static int DROP_DOWN_LIST
```


The SDT represents a drop down list when displayed in the document.

### ENTITY_PICKER {#ENTITY-PICKER}
```
public static int ENTITY_PICKER
```


The SDT represents an entity picker that allows the user to select an instance of an external content type.

 **Remarks:** 

This is MS-specific feature available since Office 2010 and not supported by the ISO/IEC 29500 OOXML standard.

### EQUATION {#EQUATION}
```
public static int EQUATION
```


The SDT represents an equation.

### GROUP {#GROUP}
```
public static int GROUP
```


The SDT represents a restricted grouping when displayed in the document.

### NONE {#NONE}
```
public static int NONE
```


No type is assigned to the SDT.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


The SDT represents a picture when displayed in the document.

### PLAIN_TEXT {#PLAIN-TEXT}
```
public static int PLAIN_TEXT
```


The SDT represents a plain text box when displayed in the document.

### REPEATING_SECTION {#REPEATING-SECTION}
```
public static int REPEATING_SECTION
```


The SDT represents repeating section type when displayed in the document.

 **Remarks:** 

This is MS-specific feature available since Office 2013 and not supported by the ISO/IEC 29500 OOXML standard.

### REPEATING_SECTION_ITEM {#REPEATING-SECTION-ITEM}
```
public static int REPEATING_SECTION_ITEM
```


The SDT represents repeating section item.

 **Remarks:** 

This is MS-specific feature available since Office 2013 and not supported by the ISO/IEC 29500 OOXML standard.

### RICH_TEXT {#RICH-TEXT}
```
public static int RICH_TEXT
```


The SDT represents a rich text box when displayed in the document.

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fromName(String sdtTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sdtTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sdtTypeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int sdtType) {#getName-int}
```
public static String getName(int sdtType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sdtType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(int sdtType) {#toString-int}
```
public static String toString(int sdtType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sdtType | int |  |

**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

