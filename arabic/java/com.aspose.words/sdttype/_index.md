---
title: "SdtType"
linktitle: "SdtType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع عقدة علامة مستند منظم SDT في Java."
type: docs
weight: 604
url: /ar/java/com.aspose.words/sdttype/
---

**Inheritance:**
java.lang.Object
```
public class SdtType
```

يحدد نوع عقدة علامة مستند مهيكلة (SDT).

 **Examples:** 

يظهر كيفية العمل مع الأنماط لعناصر التحكم بالمحتوى.

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

يظهر كيفية ملء جدول بالبيانات من جزء XML.

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

يظهر كيفية إنشاء مجموعة من علامات المستند المنظم على مستوى الصف.

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

يظهر كيفية إنشاء علامة مستند منظم من نوع الاقتباس.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [BIBLIOGRAPHY](#BIBLIOGRAPHY) | تمثل الـ SDT إدخالًا في الببليوغرافيا. |
| [BUILDING_BLOCK_GALLERY](#BUILDING-BLOCK-GALLERY) | تمثل الـ SDT نوع معرض كتل البناء. |
| [CHECKBOX](#CHECKBOX) | تمثل الـ SDT خانة اختيار عند عرضها في المستند. |
| [CITATION](#CITATION) | تمثل الـ SDT اقتباسًا. |
| [COMBO_BOX](#COMBO-BOX) | تمثل الـ SDT مربعًا مركبًا عند عرضها في المستند. |
| [DATE](#DATE) | تمثل الـ SDT أداة اختيار تاريخ عند عرضها في المستند. |
| [DOC_PART_OBJ](#DOC-PART-OBJ) | تمثل الـ SDT نوع جزء المستند. |
| [DROP_DOWN_LIST](#DROP-DOWN-LIST) | تمثل الـ SDT قائمة منسدلة عند عرضها في المستند. |
| [ENTITY_PICKER](#ENTITY-PICKER) | تمثل الـ SDT أداة اختيار كيان تسمح للمستخدم باختيار نسخة من نوع محتوى خارجي. |
| [EQUATION](#EQUATION) | تمثل الـ SDT معادلة. |
| [GROUP](#GROUP) | تمثل الـ SDT تجميعًا مقيدًا عند عرضها في المستند. |
| [NONE](#NONE) | لم يتم تعيين نوع للـ SDT. |
| [PICTURE](#PICTURE) | تمثل الـ SDT صورة عند عرضها في المستند. |
| [PLAIN_TEXT](#PLAIN-TEXT) | تمثل الـ SDT مربع نص عادي عند عرضها في المستند. |
| [REPEATING_SECTION](#REPEATING-SECTION) | تمثل الـ SDT نوع قسم متكرر عند عرضها في المستند. |
| [REPEATING_SECTION_ITEM](#REPEATING-SECTION-ITEM) | تمثل الـ SDT عنصر قسم متكرر. |
| [RICH_TEXT](#RICH-TEXT) | تمثل الـ SDT مربع نص غني عند عرضها في المستند. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String sdtTypeName)](#fromName-java.lang.String) |  |
| [getName(int sdtType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtType)](#toString-int) |  |
### BIBLIOGRAPHY {#BIBLIOGRAPHY}
```
public static int BIBLIOGRAPHY
```


تمثل الـ SDT إدخالًا في الببليوغرافيا.

### BUILDING_BLOCK_GALLERY {#BUILDING-BLOCK-GALLERY}
```
public static int BUILDING_BLOCK_GALLERY
```


تمثل الـ SDT نوع معرض كتل البناء.

### CHECKBOX {#CHECKBOX}
```
public static int CHECKBOX
```


تمثل الـ SDT خانة اختيار عند عرضها في المستند.

 **Remarks:** 

هذه ميزة خاصة بـ MS متاحة منذ Office 2010 ولا يدعمها معيار ISO/IEC 29500 OOXML.

### CITATION {#CITATION}
```
public static int CITATION
```


تمثل الـ SDT اقتباسًا.

### COMBO_BOX {#COMBO-BOX}
```
public static int COMBO_BOX
```


تمثل الـ SDT مربعًا مركبًا عند عرضها في المستند.

### DATE {#DATE}
```
public static int DATE
```


تمثل الـ SDT أداة اختيار تاريخ عند عرضها في المستند.

### DOC_PART_OBJ {#DOC-PART-OBJ}
```
public static int DOC_PART_OBJ
```


تمثل الـ SDT نوع جزء المستند.

### DROP_DOWN_LIST {#DROP-DOWN-LIST}
```
public static int DROP_DOWN_LIST
```


تمثل الـ SDT قائمة منسدلة عند عرضها في المستند.

### ENTITY_PICKER {#ENTITY-PICKER}
```
public static int ENTITY_PICKER
```


تمثل الـ SDT أداة اختيار كيان تسمح للمستخدم باختيار نسخة من نوع محتوى خارجي.

 **Remarks:** 

هذه ميزة خاصة بـ MS متاحة منذ Office 2010 ولا يدعمها معيار ISO/IEC 29500 OOXML.

### EQUATION {#EQUATION}
```
public static int EQUATION
```


تمثل الـ SDT معادلة.

### GROUP {#GROUP}
```
public static int GROUP
```


تمثل الـ SDT تجميعًا مقيدًا عند عرضها في المستند.

### NONE {#NONE}
```
public static int NONE
```


لم يتم تعيين نوع للـ SDT.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


تمثل الـ SDT صورة عند عرضها في المستند.

### PLAIN_TEXT {#PLAIN-TEXT}
```
public static int PLAIN_TEXT
```


تمثل الـ SDT مربع نص عادي عند عرضها في المستند.

### REPEATING_SECTION {#REPEATING-SECTION}
```
public static int REPEATING_SECTION
```


تمثل الـ SDT نوع قسم متكرر عند عرضها في المستند.

 **Remarks:** 

هذه ميزة خاصة بـ MS متاحة منذ Office 2013 ولا يدعمها معيار ISO/IEC 29500 OOXML.

### REPEATING_SECTION_ITEM {#REPEATING-SECTION-ITEM}
```
public static int REPEATING_SECTION_ITEM
```


تمثل الـ SDT عنصر قسم متكرر.

 **Remarks:** 

هذه ميزة خاصة بـ MS متاحة منذ Office 2013 ولا يدعمها معيار ISO/IEC 29500 OOXML.

### RICH_TEXT {#RICH-TEXT}
```
public static int RICH_TEXT
```


تمثل الـ SDT مربع نص غني عند عرضها في المستند.

### length {#length}
```
public static int length
```


### fromName(String sdtTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sdtTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sdtTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sdtType) {#getName-int}
```
public static String getName(int sdtType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| sdtType | int |  |

**Returns:**
java.lang.String
