---
title: "MarkupLevel"
linktitle: "MarkupLevel"
second_title: "Aspose.Words per Java"
description: "Specifica il livello nell'albero del documento in cui può comparire un particolare StructuredDocumentTag in Java."
type: docs
weight: 458
url: /it/java/com.aspose.words/markuplevel/
---

**Inheritance:**
java.lang.Object
```
public class MarkupLevel
```

Specifica il livello nell'albero del documento in cui può comparire un particolare [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/).

 **Examples:** 

Mostra come lavorare con gli stili per gli elementi di controllo del contenuto.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [BLOCK](#BLOCK) | L'elemento si verifica a livello di blocco (ad es. |
| [CELL](#CELL) | L'elemento si verifica tra le celle in una riga. |
| [INLINE](#INLINE) | L'elemento si verifica a livello inline (ad es. |
| [ROW](#ROW) | L'elemento si verifica tra le righe in una tabella. |
| [UNKNOWN](#UNKNOWN) | Specifica il valore sconosciuto o non valido. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String markupLevelName)](#fromName-java.lang.String) |  |
| [getName(int markupLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markupLevel)](#toString-int) |  |
### BLOCK {#BLOCK}
```
public static int BLOCK
```


L'elemento si verifica a livello di blocco (ad es. tra tabelle e paragrafi).

### CELL {#CELL}
```
public static int CELL
```


L'elemento si verifica tra le celle in una riga.

### INLINE {#INLINE}
```
public static int INLINE
```


L'elemento si verifica a livello inline (ad es. tra sequenze di testo).

### ROW {#ROW}
```
public static int ROW
```


L'elemento si verifica tra le righe in una tabella.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Specifica il valore sconosciuto o non valido.

### length {#length}
```
public static int length
```


### fromName(String markupLevelName) {#fromName-java.lang.String}
```
public static int fromName(String markupLevelName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| markupLevelName | java.lang.String |  |

**Returns:**
int
### getName(int markupLevel) {#getName-int}
```
public static String getName(int markupLevel)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| markupLevel | int |  |

**Returns:**
java.lang.String
