---
title: "MarkupLevel"
linktitle: "MarkupLevel"
second_title: "Aspose.Words Java için"
description: "Java'da belirli bir StructuredDocumentTag'in ortaya çıkabileceği belge ağacındaki seviyeyi belirtir."
type: docs
weight: 458
url: /tr/java/com.aspose.words/markuplevel/
---

**Inheritance:**
java.lang.Object
```
public class MarkupLevel
```

Belirli bir [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) öğesinin ortaya çıkabileceği belge ağacındaki seviyeyi belirtir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BLOCK](#BLOCK) | Eleman blok seviyesinde meydana gelir (örneğin. |
| [CELL](#CELL) | Eleman bir satırdaki hücreler arasında meydana gelir. |
| [INLINE](#INLINE) | Eleman satır içi seviyesinde meydana gelir (örneğin. |
| [ROW](#ROW) | Eleman bir tablodaki satırlar arasında meydana gelir. |
| [UNKNOWN](#UNKNOWN) | Bilinmeyen veya geçersiz değeri belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String markupLevelName)](#fromName-java.lang.String) |  |
| [getName(int markupLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markupLevel)](#toString-int) |  |
### BLOCK {#BLOCK}
```
public static int BLOCK
```


Eleman blok seviyesinde meydana gelir (örneğin tablolar ve paragraflar arasında).

### CELL {#CELL}
```
public static int CELL
```


Eleman bir satırdaki hücreler arasında meydana gelir.

### INLINE {#INLINE}
```
public static int INLINE
```


Eleman satır içi seviyesinde meydana gelir (örneğin metin akışları arasında).

### ROW {#ROW}
```
public static int ROW
```


Eleman bir tablodaki satırlar arasında meydana gelir.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Bilinmeyen veya geçersiz değeri belirtir.

### length {#length}
```
public static int length
```


### fromName(String markupLevelName) {#fromName-java.lang.String}
```
public static int fromName(String markupLevelName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| markupLevelName | java.lang.String |  |

**Returns:**
int
### getName(int markupLevel) {#getName-int}
```
public static String getName(int markupLevel)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| markupLevel | int |  |

**Returns:**
java.lang.String
