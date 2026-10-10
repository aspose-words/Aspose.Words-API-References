---
title: "MarkupLevel"
linktitle: "MarkupLevel"
second_title: "Aspose.Words لـ Java"
description: "يحدد المستوى في شجرة المستند حيث يمكن أن يحدث StructuredDocumentTag معين في Java."
type: docs
weight: 458
url: /ar/java/com.aspose.words/markuplevel/
---

**Inheritance:**
java.lang.Object
```
public class MarkupLevel
```

يحدد المستوى في شجرة المستند حيث يمكن أن يحدث [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) معين.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [BLOCK](#BLOCK) | العنصر يحدث على مستوى الكتلة (مثلاً |
| [CELL](#CELL) | العنصر يحدث بين الخلايا في صف. |
| [INLINE](#INLINE) | العنصر يحدث على المستوى الداخلي (مثلاً |
| [ROW](#ROW) | العنصر يحدث بين الصفوف في جدول. |
| [UNKNOWN](#UNKNOWN) | يحدد القيمة غير المعروفة أو غير الصالحة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String markupLevelName)](#fromName-java.lang.String) |  |
| [getName(int markupLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markupLevel)](#toString-int) |  |
### BLOCK {#BLOCK}
```
public static int BLOCK
```


العنصر يحدث على مستوى الكتلة (مثلاً بين الجداول والفقرات).

### CELL {#CELL}
```
public static int CELL
```


العنصر يحدث بين الخلايا في صف.

### INLINE {#INLINE}
```
public static int INLINE
```


العنصر يحدث على المستوى الداخلي (مثلاً بين سلاسل النص).

### ROW {#ROW}
```
public static int ROW
```


العنصر يحدث بين الصفوف في جدول.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


يحدد القيمة غير المعروفة أو غير الصالحة.

### length {#length}
```
public static int length
```


### fromName(String markupLevelName) {#fromName-java.lang.String}
```
public static int fromName(String markupLevelName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| markupLevelName | java.lang.String |  |

**Returns:**
int
### getName(int markupLevel) {#getName-int}
```
public static String getName(int markupLevel)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| markupLevel | int |  |

**Returns:**
java.lang.String
