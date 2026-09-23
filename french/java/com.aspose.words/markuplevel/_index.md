---
title: "MarkupLevel"
linktitle: "MarkupLevel"
second_title: "Aspose.Words pour Java"
description: "Spécifie le niveau dans l'arborescence du document où une StructuredDocumentTag particulière peut apparaître en Java."
type: docs
weight: 458
url: /fr/java/com.aspose.words/markuplevel/
---

**Inheritance:**
java.lang.Object
```
public class MarkupLevel
```

Spécifie le niveau dans l'arborescence du document où une [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) particulière peut apparaître.

 **Examples:** 

Montre comment travailler avec les styles pour les éléments de contrôle de contenu.

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
## Champs

| Champ | Description |
| --- | --- |
| [BLOCK](#BLOCK) | L'élément apparaît au niveau du bloc (p. ex. |
| [CELL](#CELL) | L'élément apparaît parmi les cellules d'une ligne. |
| [INLINE](#INLINE) | L'élément apparaît au niveau en ligne (p. ex. |
| [ROW](#ROW) | L'élément apparaît parmi les lignes d'un tableau. |
| [UNKNOWN](#UNKNOWN) | Spécifie la valeur inconnue ou invalide. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String markupLevelName)](#fromName-java.lang.String) |  |
| [getName(int markupLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markupLevel)](#toString-int) |  |
### BLOCK {#BLOCK}
```
public static int BLOCK
```


L'élément apparaît au niveau du bloc (p. ex. parmi les tables et les paragraphes).

### CELL {#CELL}
```
public static int CELL
```


L'élément apparaît parmi les cellules d'une ligne.

### INLINE {#INLINE}
```
public static int INLINE
```


L'élément apparaît au niveau en ligne (p. ex. parmi des séquences de texte).

### ROW {#ROW}
```
public static int ROW
```


L'élément apparaît parmi les lignes d'un tableau.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Spécifie la valeur inconnue ou invalide.

### length {#length}
```
public static int length
```


### fromName(String markupLevelName) {#fromName-java.lang.String}
```
public static int fromName(String markupLevelName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| markupLevelName | java.lang.String |  |

**Returns:**
int
### getName(int markupLevel) {#getName-int}
```
public static String getName(int markupLevel)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| markupLevel | int |  |

**Returns:**
java.lang.String
