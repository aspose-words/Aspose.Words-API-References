---
title: "SdtType"
linktitle: "SdtType"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de un nodo de etiqueta de documento estructurado SDT en Java."
type: docs
weight: 604
url: /es/java/com.aspose.words/sdttype/
---

**Inheritance:**
java.lang.Object
```
public class SdtType
```

Especifica el tipo de un nodo de etiqueta de documento estructurado (SDT).

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

Muestra cómo rellenar una tabla con datos de una parte XML.

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

Muestra cómo crear una etiqueta de documento estructurado de grupo a nivel de fila.

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

Muestra cómo crear una etiqueta de documento estructurado del tipo Cita.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [BIBLIOGRAPHY](#BIBLIOGRAPHY) | El SDT representa una entrada de bibliografía. |
| [BUILDING_BLOCK_GALLERY](#BUILDING-BLOCK-GALLERY) | El SDT representa un tipo de galería de bloques de construcción. |
| [CHECKBOX](#CHECKBOX) | El SDT representa una casilla de verificación cuando se muestra en el documento. |
| [CITATION](#CITATION) | El SDT representa una cita. |
| [COMBO_BOX](#COMBO-BOX) | El SDT representa un cuadro combinado cuando se muestra en el documento. |
| [DATE](#DATE) | El SDT representa un selector de fecha cuando se muestra en el documento. |
| [DOC_PART_OBJ](#DOC-PART-OBJ) | El SDT representa un tipo de parte de documento. |
| [DROP_DOWN_LIST](#DROP-DOWN-LIST) | El SDT representa una lista desplegable cuando se muestra en el documento. |
| [ENTITY_PICKER](#ENTITY-PICKER) | El SDT representa un selector de entidad que permite al usuario seleccionar una instancia de un tipo de contenido externo. |
| [EQUATION](#EQUATION) | El SDT representa una ecuación. |
| [GROUP](#GROUP) | El SDT representa una agrupación restringida cuando se muestra en el documento. |
| [NONE](#NONE) | No se asigna ningún tipo al SDT. |
| [PICTURE](#PICTURE) | El SDT representa una imagen cuando se muestra en el documento. |
| [PLAIN_TEXT](#PLAIN-TEXT) | El SDT representa un cuadro de texto sin formato cuando se muestra en el documento. |
| [REPEATING_SECTION](#REPEATING-SECTION) | El SDT representa un tipo de sección repetitiva cuando se muestra en el documento. |
| [REPEATING_SECTION_ITEM](#REPEATING-SECTION-ITEM) | El SDT representa un elemento de sección repetitiva. |
| [RICH_TEXT](#RICH-TEXT) | El SDT representa un cuadro de texto enriquecido cuando se muestra en el documento. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String sdtTypeName)](#fromName-java.lang.String) |  |
| [getName(int sdtType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtType)](#toString-int) |  |
### BIBLIOGRAPHY {#BIBLIOGRAPHY}
```
public static int BIBLIOGRAPHY
```


El SDT representa una entrada de bibliografía.

### BUILDING_BLOCK_GALLERY {#BUILDING-BLOCK-GALLERY}
```
public static int BUILDING_BLOCK_GALLERY
```


El SDT representa un tipo de galería de bloques de construcción.

### CHECKBOX {#CHECKBOX}
```
public static int CHECKBOX
```


El SDT representa una casilla de verificación cuando se muestra en el documento.

 **Remarks:** 

Esta es una característica específica de MS disponible desde Office 2010 y no compatible con el estándar ISO/IEC 29500 OOXML.

### CITATION {#CITATION}
```
public static int CITATION
```


El SDT representa una cita.

### COMBO_BOX {#COMBO-BOX}
```
public static int COMBO_BOX
```


El SDT representa un cuadro combinado cuando se muestra en el documento.

### DATE {#DATE}
```
public static int DATE
```


El SDT representa un selector de fecha cuando se muestra en el documento.

### DOC_PART_OBJ {#DOC-PART-OBJ}
```
public static int DOC_PART_OBJ
```


El SDT representa un tipo de parte de documento.

### DROP_DOWN_LIST {#DROP-DOWN-LIST}
```
public static int DROP_DOWN_LIST
```


El SDT representa una lista desplegable cuando se muestra en el documento.

### ENTITY_PICKER {#ENTITY-PICKER}
```
public static int ENTITY_PICKER
```


El SDT representa un selector de entidad que permite al usuario seleccionar una instancia de un tipo de contenido externo.

 **Remarks:** 

Esta es una característica específica de MS disponible desde Office 2010 y no compatible con el estándar ISO/IEC 29500 OOXML.

### EQUATION {#EQUATION}
```
public static int EQUATION
```


El SDT representa una ecuación.

### GROUP {#GROUP}
```
public static int GROUP
```


El SDT representa una agrupación restringida cuando se muestra en el documento.

### NONE {#NONE}
```
public static int NONE
```


No se asigna ningún tipo al SDT.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


El SDT representa una imagen cuando se muestra en el documento.

### PLAIN_TEXT {#PLAIN-TEXT}
```
public static int PLAIN_TEXT
```


El SDT representa un cuadro de texto sin formato cuando se muestra en el documento.

### REPEATING_SECTION {#REPEATING-SECTION}
```
public static int REPEATING_SECTION
```


El SDT representa un tipo de sección repetitiva cuando se muestra en el documento.

 **Remarks:** 

Esta es una característica específica de MS disponible desde Office 2013 y no compatible con el estándar ISO/IEC 29500 OOXML.

### REPEATING_SECTION_ITEM {#REPEATING-SECTION-ITEM}
```
public static int REPEATING_SECTION_ITEM
```


El SDT representa un elemento de sección repetitiva.

 **Remarks:** 

Esta es una característica específica de MS disponible desde Office 2013 y no compatible con el estándar ISO/IEC 29500 OOXML.

### RICH_TEXT {#RICH-TEXT}
```
public static int RICH_TEXT
```


El SDT representa un cuadro de texto enriquecido cuando se muestra en el documento.

### length {#length}
```
public static int length
```


### fromName(String sdtTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sdtTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sdtTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sdtType) {#getName-int}
```
public static String getName(int sdtType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sdtType | int |  |

**Returns:**
java.lang.String
