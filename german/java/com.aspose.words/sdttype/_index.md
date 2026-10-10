---
title: "SdtType"
linktitle: "SdtType"
second_title: "Aspose.Words für Java"
description: "Gibt den Typ eines strukturierten Dokument‑Tags SDT‑Knotens in Java an."
type: docs
weight: 604
url: /de/java/com.aspose.words/sdttype/
---

**Inheritance:**
java.lang.Object
```
public class SdtType
```

Gibt den Typ eines strukturierten Dokumenttags‑Knotens (SDT) an.

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

Zeigt, wie man eine Tabelle mit Daten aus einem XML‑Teil füllt.

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

Zeigt, wie man ein gruppiertes strukturiertes Dokument‑Tag auf Zeilenebene erstellt.

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

Zeigt, wie man ein strukturiertes Dokument‑Tag vom Typ Zitat erstellt.

```

 Document doc = new Document();

 StructuredDocumentTag sdt = new StructuredDocumentTag(doc, SdtType.CITATION, MarkupLevel.INLINE);
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 paragraph.appendChild(sdt);

 // Create a Citation field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToParagraph(0, -1);
 builder.insertField("CITATION Ath22 \\l 1033 ", "(John Lennon, 2022)");

 // Move the field to the structured document tag.
 while (sdt.getNextSibling() != null)
     sdt.appendChild(sdt.getNextSibling());

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Citation.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BIBLIOGRAPHY](#BIBLIOGRAPHY) | Das SDT stellt einen Bibliografieeintrag dar. |
| [BUILDING_BLOCK_GALLERY](#BUILDING-BLOCK-GALLERY) | Das SDT stellt einen Baustein‑Galerietyp dar. |
| [CHECKBOX](#CHECKBOX) | Das SDT stellt ein Kontrollkästchen dar, wenn es im Dokument angezeigt wird. |
| [CITATION](#CITATION) | Das SDT stellt ein Zitat dar. |
| [COMBO_BOX](#COMBO-BOX) | Das SDT stellt ein Kombinationsfeld dar, wenn es im Dokument angezeigt wird. |
| [DATE](#DATE) | Das SDT stellt einen Datumswähler dar, wenn es im Dokument angezeigt wird. |
| [DOC_PART_OBJ](#DOC-PART-OBJ) | Das SDT stellt einen Dokumentteiltyp dar. |
| [DROP_DOWN_LIST](#DROP-DOWN-LIST) | Das SDT stellt eine Dropdown‑Liste dar, wenn es im Dokument angezeigt wird. |
| [ENTITY_PICKER](#ENTITY-PICKER) | Das SDT stellt einen Entitätsauswähler dar, der es dem Benutzer ermöglicht, eine Instanz eines externen Inhaltstyps auszuwählen. |
| [EQUATION](#EQUATION) | Das SDT stellt eine Gleichung dar. |
| [GROUP](#GROUP) | Das SDT stellt eine eingeschränkte Gruppierung dar, wenn es im Dokument angezeigt wird. |
| [NONE](#NONE) | Dem SDT ist kein Typ zugewiesen. |
| [PICTURE](#PICTURE) | Das SDT stellt ein Bild dar, wenn es im Dokument angezeigt wird. |
| [PLAIN_TEXT](#PLAIN-TEXT) | Das SDT stellt ein einfaches Textfeld dar, wenn es im Dokument angezeigt wird. |
| [REPEATING_SECTION](#REPEATING-SECTION) | Das SDT stellt einen wiederholenden Abschnittstyp dar, wenn es im Dokument angezeigt wird. |
| [REPEATING_SECTION_ITEM](#REPEATING-SECTION-ITEM) | Das SDT stellt ein wiederholendes Abschnittselement dar. |
| [RICH_TEXT](#RICH-TEXT) | Das SDT stellt ein Rich‑Text‑Feld dar, wenn es im Dokument angezeigt wird. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String sdtTypeName)](#fromName-java.lang.String) |  |
| [getName(int sdtType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtType)](#toString-int) |  |
### BIBLIOGRAPHY {#BIBLIOGRAPHY}
```
public static int BIBLIOGRAPHY
```


Das SDT stellt einen Bibliografieeintrag dar.

### BUILDING_BLOCK_GALLERY {#BUILDING-BLOCK-GALLERY}
```
public static int BUILDING_BLOCK_GALLERY
```


Das SDT stellt einen Baustein‑Galerietyp dar.

### CHECKBOX {#CHECKBOX}
```
public static int CHECKBOX
```


Das SDT stellt ein Kontrollkästchen dar, wenn es im Dokument angezeigt wird.

 **Remarks:** 

Dies ist ein MS‑spezifisches Feature, das seit Office 2010 verfügbar ist und vom ISO/IEC‑29500‑OOXML‑Standard nicht unterstützt wird.

### CITATION {#CITATION}
```
public static int CITATION
```


Das SDT stellt ein Zitat dar.

### COMBO_BOX {#COMBO-BOX}
```
public static int COMBO_BOX
```


Das SDT stellt ein Kombinationsfeld dar, wenn es im Dokument angezeigt wird.

### DATE {#DATE}
```
public static int DATE
```


Das SDT stellt einen Datumswähler dar, wenn es im Dokument angezeigt wird.

### DOC_PART_OBJ {#DOC-PART-OBJ}
```
public static int DOC_PART_OBJ
```


Das SDT stellt einen Dokumentteiltyp dar.

### DROP_DOWN_LIST {#DROP-DOWN-LIST}
```
public static int DROP_DOWN_LIST
```


Das SDT stellt eine Dropdown‑Liste dar, wenn es im Dokument angezeigt wird.

### ENTITY_PICKER {#ENTITY-PICKER}
```
public static int ENTITY_PICKER
```


Das SDT stellt einen Entitätsauswähler dar, der es dem Benutzer ermöglicht, eine Instanz eines externen Inhaltstyps auszuwählen.

 **Remarks:** 

Dies ist ein MS‑spezifisches Feature, das seit Office 2010 verfügbar ist und vom ISO/IEC‑29500‑OOXML‑Standard nicht unterstützt wird.

### EQUATION {#EQUATION}
```
public static int EQUATION
```


Das SDT stellt eine Gleichung dar.

### GROUP {#GROUP}
```
public static int GROUP
```


Das SDT stellt eine eingeschränkte Gruppierung dar, wenn es im Dokument angezeigt wird.

### NONE {#NONE}
```
public static int NONE
```


Dem SDT ist kein Typ zugewiesen.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


Das SDT stellt ein Bild dar, wenn es im Dokument angezeigt wird.

### PLAIN_TEXT {#PLAIN-TEXT}
```
public static int PLAIN_TEXT
```


Das SDT stellt ein einfaches Textfeld dar, wenn es im Dokument angezeigt wird.

### REPEATING_SECTION {#REPEATING-SECTION}
```
public static int REPEATING_SECTION
```


Das SDT stellt einen wiederholenden Abschnittstyp dar, wenn es im Dokument angezeigt wird.

 **Remarks:** 

Dies ist ein MS‑spezifisches Feature, das seit Office 2013 verfügbar ist und vom ISO/IEC‑29500‑OOXML‑Standard nicht unterstützt wird.

### REPEATING_SECTION_ITEM {#REPEATING-SECTION-ITEM}
```
public static int REPEATING_SECTION_ITEM
```


Das SDT stellt ein wiederholendes Abschnittselement dar.

 **Remarks:** 

Dies ist ein MS‑spezifisches Feature, das seit Office 2013 verfügbar ist und vom ISO/IEC‑29500‑OOXML‑Standard nicht unterstützt wird.

### RICH_TEXT {#RICH-TEXT}
```
public static int RICH_TEXT
```


Das SDT stellt ein Rich‑Text‑Feld dar, wenn es im Dokument angezeigt wird.

### length {#length}
```
public static int length
```


### fromName(String sdtTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sdtTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sdtTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sdtType) {#getName-int}
```
public static String getName(int sdtType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
### toString(int sdtType) {#toString-int}
```
public static String toString(int sdtType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sdtType | int |  |

**Returns:**
java.lang.String
