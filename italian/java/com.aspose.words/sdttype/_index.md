---
title: "SdtType"
linktitle: "SdtType"
second_title: "Aspose.Words per Java"
description: "Specifica il tipo di un nodo tag documento strutturato SDT in Java."
type: docs
weight: 604
url: /it/java/com.aspose.words/sdttype/
---

**Inheritance:**
java.lang.Object
```
public class SdtType
```

Specifica il tipo di nodo di un tag di documento strutturato (SDT).

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

Mostra come riempire una tabella con i dati da una parte XML.

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

Mostra come creare un tag documento strutturato di gruppo a livello di riga.

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

Mostra come creare un tag documento strutturato di tipo Citazione.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [BIBLIOGRAPHY](#BIBLIOGRAPHY) | Il SDT rappresenta una voce di bibliografia. |
| [BUILDING_BLOCK_GALLERY](#BUILDING-BLOCK-GALLERY) | Il SDT rappresenta un tipo di galleria di blocchi di costruzione. |
| [CHECKBOX](#CHECKBOX) | Il SDT rappresenta una casella di controllo quando visualizzato nel documento. |
| [CITATION](#CITATION) | Il SDT rappresenta una citazione. |
| [COMBO_BOX](#COMBO-BOX) | Il SDT rappresenta una casella combinata quando visualizzato nel documento. |
| [DATE](#DATE) | Il SDT rappresenta un selettore di data quando visualizzato nel documento. |
| [DOC_PART_OBJ](#DOC-PART-OBJ) | Il SDT rappresenta un tipo di parte del documento. |
| [DROP_DOWN_LIST](#DROP-DOWN-LIST) | Il SDT rappresenta un elenco a discesa quando visualizzato nel documento. |
| [ENTITY_PICKER](#ENTITY-PICKER) | Il SDT rappresenta un selettore di entità che consente all'utente di selezionare un'istanza di un tipo di contenuto esterno. |
| [EQUATION](#EQUATION) | Il SDT rappresenta un'equazione. |
| [GROUP](#GROUP) | Il SDT rappresenta un raggruppamento ristretto quando visualizzato nel documento. |
| [NONE](#NONE) | Nessun tipo è assegnato al SDT. |
| [PICTURE](#PICTURE) | Il SDT rappresenta un'immagine quando visualizzato nel documento. |
| [PLAIN_TEXT](#PLAIN-TEXT) | Il SDT rappresenta una casella di testo semplice quando visualizzato nel documento. |
| [REPEATING_SECTION](#REPEATING-SECTION) | Il SDT rappresenta un tipo di sezione ripetuta quando visualizzato nel documento. |
| [REPEATING_SECTION_ITEM](#REPEATING-SECTION-ITEM) | Il SDT rappresenta un elemento di sezione ripetuta. |
| [RICH_TEXT](#RICH-TEXT) | Il SDT rappresenta una casella di testo formattato quando visualizzato nel documento. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String sdtTypeName)](#fromName-java.lang.String) |  |
| [getName(int sdtType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtType)](#toString-int) |  |
### BIBLIOGRAPHY {#BIBLIOGRAPHY}
```
public static int BIBLIOGRAPHY
```


Il SDT rappresenta una voce di bibliografia.

### BUILDING_BLOCK_GALLERY {#BUILDING-BLOCK-GALLERY}
```
public static int BUILDING_BLOCK_GALLERY
```


Il SDT rappresenta un tipo di galleria di blocchi di costruzione.

### CHECKBOX {#CHECKBOX}
```
public static int CHECKBOX
```


Il SDT rappresenta una casella di controllo quando visualizzato nel documento.

 **Remarks:** 

Questa è una funzionalità specifica di MS disponibile a partire da Office 2010 e non supportata dallo standard ISO/IEC 29500 OOXML.

### CITATION {#CITATION}
```
public static int CITATION
```


Il SDT rappresenta una citazione.

### COMBO_BOX {#COMBO-BOX}
```
public static int COMBO_BOX
```


Il SDT rappresenta una casella combinata quando visualizzato nel documento.

### DATE {#DATE}
```
public static int DATE
```


Il SDT rappresenta un selettore di data quando visualizzato nel documento.

### DOC_PART_OBJ {#DOC-PART-OBJ}
```
public static int DOC_PART_OBJ
```


Il SDT rappresenta un tipo di parte del documento.

### DROP_DOWN_LIST {#DROP-DOWN-LIST}
```
public static int DROP_DOWN_LIST
```


Il SDT rappresenta un elenco a discesa quando visualizzato nel documento.

### ENTITY_PICKER {#ENTITY-PICKER}
```
public static int ENTITY_PICKER
```


Il SDT rappresenta un selettore di entità che consente all'utente di selezionare un'istanza di un tipo di contenuto esterno.

 **Remarks:** 

Questa è una funzionalità specifica di MS disponibile a partire da Office 2010 e non supportata dallo standard ISO/IEC 29500 OOXML.

### EQUATION {#EQUATION}
```
public static int EQUATION
```


Il SDT rappresenta un'equazione.

### GROUP {#GROUP}
```
public static int GROUP
```


Il SDT rappresenta un raggruppamento ristretto quando visualizzato nel documento.

### NONE {#NONE}
```
public static int NONE
```


Nessun tipo è assegnato al SDT.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


Il SDT rappresenta un'immagine quando visualizzato nel documento.

### PLAIN_TEXT {#PLAIN-TEXT}
```
public static int PLAIN_TEXT
```


Il SDT rappresenta una casella di testo semplice quando visualizzato nel documento.

### REPEATING_SECTION {#REPEATING-SECTION}
```
public static int REPEATING_SECTION
```


Il SDT rappresenta un tipo di sezione ripetuta quando visualizzato nel documento.

 **Remarks:** 

Questa è una funzionalità specifica di MS disponibile a partire da Office 2013 e non supportata dallo standard ISO/IEC 29500 OOXML.

### REPEATING_SECTION_ITEM {#REPEATING-SECTION-ITEM}
```
public static int REPEATING_SECTION_ITEM
```


Il SDT rappresenta un elemento di sezione ripetuta.

 **Remarks:** 

Questa è una funzionalità specifica di MS disponibile a partire da Office 2013 e non supportata dallo standard ISO/IEC 29500 OOXML.

### RICH_TEXT {#RICH-TEXT}
```
public static int RICH_TEXT
```


Il SDT rappresenta una casella di testo formattato quando visualizzato nel documento.

### length {#length}
```
public static int length
```


### fromName(String sdtTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sdtTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sdtTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sdtType) {#getName-int}
```
public static String getName(int sdtType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sdtType | int |  |

**Returns:**
java.lang.String
