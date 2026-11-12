---
title: "MarkupLevel"
linktitle: "MarkupLevel"
second_title: "Aspose.Words для Java"
description: "Указывает уровень в дереве документа, где может возникать конкретный StructuredDocumentTag в Java."
type: docs
weight: 458
url: /ru/java/com.aspose.words/markuplevel/
---

**Inheritance:**
java.lang.Object
```
public class MarkupLevel
```

Указывает уровень в дереве документа, где может возникать конкретный [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/).

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
## Поля

| Поле | Описание |
| --- | --- |
| [BLOCK](#BLOCK) | Элемент находится на уровне блока (например, |
| [CELL](#CELL) | Элемент находится среди ячеек в строке. |
| [INLINE](#INLINE) | Элемент находится на уровне встроенного (например, |
| [ROW](#ROW) | Элемент находится среди строк в таблице. |
| [UNKNOWN](#UNKNOWN) | Указывает неизвестное или недопустимое значение. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String markupLevelName)](#fromName-java.lang.String) |  |
| [getName(int markupLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markupLevel)](#toString-int) |  |
### BLOCK {#BLOCK}
```
public static int BLOCK
```


Элемент находится на уровне блока (например, среди таблиц и абзацев).

### CELL {#CELL}
```
public static int CELL
```


Элемент находится среди ячеек в строке.

### INLINE {#INLINE}
```
public static int INLINE
```


Элемент находится на уровне встроенного (например, среди последовательностей текста).

### ROW {#ROW}
```
public static int ROW
```


Элемент находится среди строк в таблице.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Указывает неизвестное или недопустимое значение.

### length {#length}
```
public static int length
```


### fromName(String markupLevelName) {#fromName-java.lang.String}
```
public static int fromName(String markupLevelName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| markupLevelName | java.lang.String |  |

**Returns:**
int
### getName(int markupLevel) {#getName-int}
```
public static String getName(int markupLevel)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| markupLevel | int |  |

**Returns:**
java.lang.String
