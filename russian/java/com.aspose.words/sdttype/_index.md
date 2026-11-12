---
title: "SdtType"
linktitle: "SdtType"
second_title: "Aspose.Words для Java"
description: "Указывает тип узла SDT (структурированный тег документа) в Java."
type: docs
weight: 604
url: /ru/java/com.aspose.words/sdttype/
---

**Inheritance:**
java.lang.Object
```
public class SdtType
```

Указывает тип узла структурированного тега документа (SDT).

 **Examples:** 

Показывает, как работать со стилями элементов управления содержимым.

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

Показывает, как заполнить таблицу данными из XML‑части.

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

Показывает, как создать групповой структурированный тег документа на уровне Row.

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

Показывает, как создать структурированный тег документа типа Citation.

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
## Поля

| Поле | Описание |
| --- | --- |
| [BIBLIOGRAPHY](#BIBLIOGRAPHY) | SDT представляет запись библиографии. |
| [BUILDING_BLOCK_GALLERY](#BUILDING-BLOCK-GALLERY) | SDT представляет тип галереи строительных блоков. |
| [CHECKBOX](#CHECKBOX) | SDT представляет флажок при отображении в документе. |
| [CITATION](#CITATION) | SDT представляет цитату. |
| [COMBO_BOX](#COMBO-BOX) | SDT представляет комбинированный список при отображении в документе. |
| [DATE](#DATE) | SDT представляет выбор даты при отображении в документе. |
| [DOC_PART_OBJ](#DOC-PART-OBJ) | SDT представляет тип части документа. |
| [DROP_DOWN_LIST](#DROP-DOWN-LIST) | SDT представляет выпадающий список при отображении в документе. |
| [ENTITY_PICKER](#ENTITY-PICKER) | SDT представляет средство выбора сущности, позволяющее пользователю выбрать экземпляр внешнего типа контента. |
| [EQUATION](#EQUATION) | SDT представляет уравнение. |
| [GROUP](#GROUP) | SDT представляет ограниченную группировку при отображении в документе. |
| [NONE](#NONE) | Тип не назначен SDT. |
| [PICTURE](#PICTURE) | SDT представляет изображение при отображении в документе. |
| [PLAIN_TEXT](#PLAIN-TEXT) | SDT представляет простое текстовое поле при отображении в документе. |
| [REPEATING_SECTION](#REPEATING-SECTION) | SDT представляет тип повторяющегося раздела при отображении в документе. |
| [REPEATING_SECTION_ITEM](#REPEATING-SECTION-ITEM) | SDT представляет элемент повторяющегося раздела. |
| [RICH_TEXT](#RICH-TEXT) | SDT представляет поле форматированного текста при отображении в документе. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String sdtTypeName)](#fromName-java.lang.String) |  |
| [getName(int sdtType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtType)](#toString-int) |  |
### BIBLIOGRAPHY {#BIBLIOGRAPHY}
```
public static int BIBLIOGRAPHY
```


SDT представляет запись библиографии.

### BUILDING_BLOCK_GALLERY {#BUILDING-BLOCK-GALLERY}
```
public static int BUILDING_BLOCK_GALLERY
```


SDT представляет тип галереи строительных блоков.

### CHECKBOX {#CHECKBOX}
```
public static int CHECKBOX
```


SDT представляет флажок при отображении в документе.

 **Remarks:** 

Это специфичная для Microsoft функция, доступная с Office 2010 и не поддерживаемая стандартом ISO/IEC 29500 OOXML.

### CITATION {#CITATION}
```
public static int CITATION
```


SDT представляет цитату.

### COMBO_BOX {#COMBO-BOX}
```
public static int COMBO_BOX
```


SDT представляет комбинированный список при отображении в документе.

### DATE {#DATE}
```
public static int DATE
```


SDT представляет выбор даты при отображении в документе.

### DOC_PART_OBJ {#DOC-PART-OBJ}
```
public static int DOC_PART_OBJ
```


SDT представляет тип части документа.

### DROP_DOWN_LIST {#DROP-DOWN-LIST}
```
public static int DROP_DOWN_LIST
```


SDT представляет выпадающий список при отображении в документе.

### ENTITY_PICKER {#ENTITY-PICKER}
```
public static int ENTITY_PICKER
```


SDT представляет средство выбора сущности, позволяющее пользователю выбрать экземпляр внешнего типа контента.

 **Remarks:** 

Это специфичная для Microsoft функция, доступная с Office 2010 и не поддерживаемая стандартом ISO/IEC 29500 OOXML.

### EQUATION {#EQUATION}
```
public static int EQUATION
```


SDT представляет уравнение.

### GROUP {#GROUP}
```
public static int GROUP
```


SDT представляет ограниченную группировку при отображении в документе.

### NONE {#NONE}
```
public static int NONE
```


Тип не назначен SDT.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


SDT представляет изображение при отображении в документе.

### PLAIN_TEXT {#PLAIN-TEXT}
```
public static int PLAIN_TEXT
```


SDT представляет простое текстовое поле при отображении в документе.

### REPEATING_SECTION {#REPEATING-SECTION}
```
public static int REPEATING_SECTION
```


SDT представляет тип повторяющегося раздела при отображении в документе.

 **Remarks:** 

Это специфичная для Microsoft функция, доступная с Office 2013 и не поддерживаемая стандартом ISO/IEC 29500 OOXML.

### REPEATING_SECTION_ITEM {#REPEATING-SECTION-ITEM}
```
public static int REPEATING_SECTION_ITEM
```


SDT представляет элемент повторяющегося раздела.

 **Remarks:** 

Это специфичная для Microsoft функция, доступная с Office 2013 и не поддерживаемая стандартом ISO/IEC 29500 OOXML.

### RICH_TEXT {#RICH-TEXT}
```
public static int RICH_TEXT
```


SDT представляет поле форматированного текста при отображении в документе.

### length {#length}
```
public static int length
```


### fromName(String sdtTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sdtTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sdtTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sdtType) {#getName-int}
```
public static String getName(int sdtType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| sdtType | int |  |

**Returns:**
java.lang.String
