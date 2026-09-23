---
title: "SdtType"
linktitle: "SdtType"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type d'un nœud d'étiquette de document structuré SDT en Java."
type: docs
weight: 604
url: /fr/java/com.aspose.words/sdttype/
---

**Inheritance:**
java.lang.Object
```
public class SdtType
```

Spécifie le type d'un nœud de balise de document structuré (SDT).

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

Montre comment remplir un tableau avec des données provenant d'une partie XML.

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

Montre comment créer une balise de document structuré de groupe au niveau de la ligne.

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

Montre comment créer une balise de document structuré de type Citation.

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
## Champs

| Champ | Description |
| --- | --- |
| [BIBLIOGRAPHY](#BIBLIOGRAPHY) | Le SDT représente une entrée de bibliographie. |
| [BUILDING_BLOCK_GALLERY](#BUILDING-BLOCK-GALLERY) | Le SDT représente un type de galerie de blocs de construction. |
| [CHECKBOX](#CHECKBOX) | Le SDT représente une case à cocher lorsqu'il est affiché dans le document. |
| [CITATION](#CITATION) | Le SDT représente une citation. |
| [COMBO_BOX](#COMBO-BOX) | Le SDT représente une zone combinée lorsqu'il est affiché dans le document. |
| [DATE](#DATE) | Le SDT représente un sélecteur de date lorsqu'il est affiché dans le document. |
| [DOC_PART_OBJ](#DOC-PART-OBJ) | Le SDT représente un type de partie de document. |
| [DROP_DOWN_LIST](#DROP-DOWN-LIST) | Le SDT représente une liste déroulante lorsqu'il est affiché dans le document. |
| [ENTITY_PICKER](#ENTITY-PICKER) | Le SDT représente un sélecteur d'entité qui permet à l'utilisateur de choisir une instance d'un type de contenu externe. |
| [EQUATION](#EQUATION) | Le SDT représente une équation. |
| [GROUP](#GROUP) | Le SDT représente un regroupement restreint lorsqu'il est affiché dans le document. |
| [NONE](#NONE) | Aucun type n'est attribué au SDT. |
| [PICTURE](#PICTURE) | Le SDT représente une image lorsqu'il est affiché dans le document. |
| [PLAIN_TEXT](#PLAIN-TEXT) | Le SDT représente une zone de texte simple lorsqu'il est affiché dans le document. |
| [REPEATING_SECTION](#REPEATING-SECTION) | Le SDT représente un type de section répétitive lorsqu'il est affiché dans le document. |
| [REPEATING_SECTION_ITEM](#REPEATING-SECTION-ITEM) | Le SDT représente un élément de section répétitive. |
| [RICH_TEXT](#RICH-TEXT) | Le SDT représente une zone de texte enrichi lorsqu'il est affiché dans le document. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String sdtTypeName)](#fromName-java.lang.String) |  |
| [getName(int sdtType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtType)](#toString-int) |  |
### BIBLIOGRAPHY {#BIBLIOGRAPHY}
```
public static int BIBLIOGRAPHY
```


Le SDT représente une entrée de bibliographie.

### BUILDING_BLOCK_GALLERY {#BUILDING-BLOCK-GALLERY}
```
public static int BUILDING_BLOCK_GALLERY
```


Le SDT représente un type de galerie de blocs de construction.

### CHECKBOX {#CHECKBOX}
```
public static int CHECKBOX
```


Le SDT représente une case à cocher lorsqu'il est affiché dans le document.

 **Remarks:** 

Il s'agit d'une fonctionnalité spécifique à Microsoft disponible depuis Office 2010 et non prise en charge par la norme ISO/IEC 29500 OOXML.

### CITATION {#CITATION}
```
public static int CITATION
```


Le SDT représente une citation.

### COMBO_BOX {#COMBO-BOX}
```
public static int COMBO_BOX
```


Le SDT représente une zone combinée lorsqu'il est affiché dans le document.

### DATE {#DATE}
```
public static int DATE
```


Le SDT représente un sélecteur de date lorsqu'il est affiché dans le document.

### DOC_PART_OBJ {#DOC-PART-OBJ}
```
public static int DOC_PART_OBJ
```


Le SDT représente un type de partie de document.

### DROP_DOWN_LIST {#DROP-DOWN-LIST}
```
public static int DROP_DOWN_LIST
```


Le SDT représente une liste déroulante lorsqu'il est affiché dans le document.

### ENTITY_PICKER {#ENTITY-PICKER}
```
public static int ENTITY_PICKER
```


Le SDT représente un sélecteur d'entité qui permet à l'utilisateur de choisir une instance d'un type de contenu externe.

 **Remarks:** 

Il s'agit d'une fonctionnalité spécifique à Microsoft disponible depuis Office 2010 et non prise en charge par la norme ISO/IEC 29500 OOXML.

### EQUATION {#EQUATION}
```
public static int EQUATION
```


Le SDT représente une équation.

### GROUP {#GROUP}
```
public static int GROUP
```


Le SDT représente un regroupement restreint lorsqu'il est affiché dans le document.

### NONE {#NONE}
```
public static int NONE
```


Aucun type n'est attribué au SDT.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


Le SDT représente une image lorsqu'il est affiché dans le document.

### PLAIN_TEXT {#PLAIN-TEXT}
```
public static int PLAIN_TEXT
```


Le SDT représente une zone de texte simple lorsqu'il est affiché dans le document.

### REPEATING_SECTION {#REPEATING-SECTION}
```
public static int REPEATING_SECTION
```


Le SDT représente un type de section répétitive lorsqu'il est affiché dans le document.

 **Remarks:** 

Il s'agit d'une fonctionnalité spécifique à Microsoft disponible depuis Office 2013 et non prise en charge par la norme ISO/IEC 29500 OOXML.

### REPEATING_SECTION_ITEM {#REPEATING-SECTION-ITEM}
```
public static int REPEATING_SECTION_ITEM
```


Le SDT représente un élément de section répétitive.

 **Remarks:** 

Il s'agit d'une fonctionnalité spécifique à Microsoft disponible depuis Office 2013 et non prise en charge par la norme ISO/IEC 29500 OOXML.

### RICH_TEXT {#RICH-TEXT}
```
public static int RICH_TEXT
```


Le SDT représente une zone de texte enrichi lorsqu'il est affiché dans le document.

### length {#length}
```
public static int length
```


### fromName(String sdtTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sdtTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sdtTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sdtType) {#getName-int}
```
public static String getName(int sdtType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| sdtType | int |  |

**Returns:**
java.lang.String
