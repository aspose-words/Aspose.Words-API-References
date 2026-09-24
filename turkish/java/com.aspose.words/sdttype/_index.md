---
title: "SdtType"
linktitle: "SdtType"
second_title: "Aspose.Words Java için"
description: "Java'da yapılandırılmış belge etiketi SDT düğümünün türünü belirtir."
type: docs
weight: 604
url: /tr/java/com.aspose.words/sdttype/
---

**Inheritance:**
java.lang.Object
```
public class SdtType
```

Bir yapılandırılmış belge etiketi (SDT) düğümünün türünü belirtir.

 **Examples:** 

İçerik denetimi öğeleri için stillerle nasıl çalışılacağını gösterir.

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

Bir XML bölümünden veri ile tabloyu nasıl dolduracağınızı gösterir.

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

Satır seviyesinde grup yapılandırılmış belge etiketi oluşturmayı gösterir.

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

Alıntı türünde bir yapılandırılmış belge etiketi oluşturmayı gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BIBLIOGRAPHY](#BIBLIOGRAPHY) | SDT bir bibliyografya girişini temsil eder. |
| [BUILDING_BLOCK_GALLERY](#BUILDING-BLOCK-GALLERY) | SDT bir yapı bloğu galeri türünü temsil eder. |
| [CHECKBOX](#CHECKBOX) | SDT belgede görüntülendiğinde bir onay kutusunu temsil eder. |
| [CITATION](#CITATION) | SDT bir alıntıyı temsil eder. |
| [COMBO_BOX](#COMBO-BOX) | SDT belgede görüntülendiğinde bir birleşik kutuyu temsil eder. |
| [DATE](#DATE) | SDT belgede görüntülendiğinde bir tarih seçiciyi temsil eder. |
| [DOC_PART_OBJ](#DOC-PART-OBJ) | SDT bir belge parçası türünü temsil eder. |
| [DROP_DOWN_LIST](#DROP-DOWN-LIST) | SDT belgede görüntülendiğinde bir açılır listeyi temsil eder. |
| [ENTITY_PICKER](#ENTITY-PICKER) | SDT, kullanıcının harici bir içerik türünün örneğini seçmesine izin veren bir varlık seçiciyi temsil eder. |
| [EQUATION](#EQUATION) | SDT bir denklemi temsil eder. |
| [GROUP](#GROUP) | SDT belgede görüntülendiğinde sınırlı bir gruplamayı temsil eder. |
| [NONE](#NONE) | SDT'ye bir tür atanmadı. |
| [PICTURE](#PICTURE) | SDT belgede görüntülendiğinde bir resmi temsil eder. |
| [PLAIN_TEXT](#PLAIN-TEXT) | SDT belgede görüntülendiğinde düz metin kutusunu temsil eder. |
| [REPEATING_SECTION](#REPEATING-SECTION) | SDT belgede görüntülendiğinde yinelenen bölüm türünü temsil eder. |
| [REPEATING_SECTION_ITEM](#REPEATING-SECTION-ITEM) | SDT yinelenen bölüm öğesini temsil eder. |
| [RICH_TEXT](#RICH-TEXT) | SDT belgede görüntülendiğinde zengin metin kutusunu temsil eder. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String sdtTypeName)](#fromName-java.lang.String) |  |
| [getName(int sdtType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtType)](#toString-int) |  |
### BIBLIOGRAPHY {#BIBLIOGRAPHY}
```
public static int BIBLIOGRAPHY
```


SDT bir bibliyografya girişini temsil eder.

### BUILDING_BLOCK_GALLERY {#BUILDING-BLOCK-GALLERY}
```
public static int BUILDING_BLOCK_GALLERY
```


SDT bir yapı bloğu galeri türünü temsil eder.

### CHECKBOX {#CHECKBOX}
```
public static int CHECKBOX
```


SDT belgede görüntülendiğinde bir onay kutusunu temsil eder.

 **Remarks:** 

Bu, Office 2010'dan beri mevcut olan ve ISO/IEC 29500 OOXML standardı tarafından desteklenmeyen MS'ye özgü bir özelliktir.

### CITATION {#CITATION}
```
public static int CITATION
```


SDT bir alıntıyı temsil eder.

### COMBO_BOX {#COMBO-BOX}
```
public static int COMBO_BOX
```


SDT belgede görüntülendiğinde bir birleşik kutuyu temsil eder.

### DATE {#DATE}
```
public static int DATE
```


SDT belgede görüntülendiğinde bir tarih seçiciyi temsil eder.

### DOC_PART_OBJ {#DOC-PART-OBJ}
```
public static int DOC_PART_OBJ
```


SDT bir belge parçası türünü temsil eder.

### DROP_DOWN_LIST {#DROP-DOWN-LIST}
```
public static int DROP_DOWN_LIST
```


SDT belgede görüntülendiğinde bir açılır listeyi temsil eder.

### ENTITY_PICKER {#ENTITY-PICKER}
```
public static int ENTITY_PICKER
```


SDT, kullanıcının harici bir içerik türünün örneğini seçmesine izin veren bir varlık seçiciyi temsil eder.

 **Remarks:** 

Bu, Office 2010'dan beri mevcut olan ve ISO/IEC 29500 OOXML standardı tarafından desteklenmeyen MS'ye özgü bir özelliktir.

### EQUATION {#EQUATION}
```
public static int EQUATION
```


SDT bir denklemi temsil eder.

### GROUP {#GROUP}
```
public static int GROUP
```


SDT belgede görüntülendiğinde sınırlı bir gruplamayı temsil eder.

### NONE {#NONE}
```
public static int NONE
```


SDT'ye bir tür atanmadı.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


SDT belgede görüntülendiğinde bir resmi temsil eder.

### PLAIN_TEXT {#PLAIN-TEXT}
```
public static int PLAIN_TEXT
```


SDT belgede görüntülendiğinde düz metin kutusunu temsil eder.

### REPEATING_SECTION {#REPEATING-SECTION}
```
public static int REPEATING_SECTION
```


SDT belgede görüntülendiğinde yinelenen bölüm türünü temsil eder.

 **Remarks:** 

Bu, Office 2013'ten beri mevcut olan ve ISO/IEC 29500 OOXML standardı tarafından desteklenmeyen MS'ye özgü bir özelliktir.

### REPEATING_SECTION_ITEM {#REPEATING-SECTION-ITEM}
```
public static int REPEATING_SECTION_ITEM
```


SDT yinelenen bölüm öğesini temsil eder.

 **Remarks:** 

Bu, Office 2013'ten beri mevcut olan ve ISO/IEC 29500 OOXML standardı tarafından desteklenmeyen MS'ye özgü bir özelliktir.

### RICH_TEXT {#RICH-TEXT}
```
public static int RICH_TEXT
```


SDT belgede görüntülendiğinde zengin metin kutusunu temsil eder.

### length {#length}
```
public static int length
```


### fromName(String sdtTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sdtTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sdtTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sdtType) {#getName-int}
```
public static String getName(int sdtType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sdtType | int |  |

**Returns:**
java.lang.String
