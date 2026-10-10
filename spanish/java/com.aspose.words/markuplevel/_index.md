---
title: "MarkupLevel"
linktitle: "MarkupLevel"
second_title: "Aspose.Words para Java"
description: "Especifica el nivel en el árbol del documento donde puede aparecer un StructuredDocumentTag particular en Java."
type: docs
weight: 458
url: /es/java/com.aspose.words/markuplevel/
---

**Inheritance:**
java.lang.Object
```
public class MarkupLevel
```

Especifica el nivel en el árbol del documento donde puede aparecer un [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) particular.

 **Examples:** 

Muestra cómo trabajar con estilos para elementos de control de contenido.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [BLOCK](#BLOCK) | El elemento ocurre a nivel de bloque (p.ej. |
| [CELL](#CELL) | El elemento ocurre entre celdas en una fila. |
| [INLINE](#INLINE) | El elemento ocurre a nivel en línea (p.ej. |
| [ROW](#ROW) | El elemento ocurre entre filas en una tabla. |
| [UNKNOWN](#UNKNOWN) | Especifica el valor desconocido o inválido. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String markupLevelName)](#fromName-java.lang.String) |  |
| [getName(int markupLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markupLevel)](#toString-int) |  |
### BLOCK {#BLOCK}
```
public static int BLOCK
```


El elemento ocurre a nivel de bloque (p.ej. entre tablas y párrafos).

### CELL {#CELL}
```
public static int CELL
```


El elemento ocurre entre celdas en una fila.

### INLINE {#INLINE}
```
public static int INLINE
```


El elemento ocurre a nivel en línea (p.ej. entre secuencias de texto).

### ROW {#ROW}
```
public static int ROW
```


El elemento ocurre entre filas en una tabla.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Especifica el valor desconocido o inválido.

### length {#length}
```
public static int length
```


### fromName(String markupLevelName) {#fromName-java.lang.String}
```
public static int fromName(String markupLevelName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| markupLevelName | java.lang.String |  |

**Returns:**
int
### getName(int markupLevel) {#getName-int}
```
public static String getName(int markupLevel)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| markupLevel | int |  |

**Returns:**
java.lang.String
