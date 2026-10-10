---
title: "FootnotePosition"
linktitle: "FootnotePosition"
second_title: "Aspose.Words per Java"
description: "Definisce la posizione della nota a piè di pagina in Java."
type: docs
weight: 342
url: /it/java/com.aspose.words/footnoteposition/
---

**Inheritance:**
java.lang.Object
```
public class FootnotePosition
```

Definisce la posizione della nota a piè di pagina.

 **Examples:** 

Mostra come selezionare un luogo diverso in cui il documento raccoglie e visualizza le sue note a piè di pagina.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A footnote is a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote.
 // Each footnote also creates an entry at the bottom of the page, consisting of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertFootnote" method.
 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote contents.");

 // We can use the "Position" property to determine where the document will place all its footnotes.
 // If we set the value of the "Position" property to "FootnotePosition.BottomOfPage",
 // every footnote will show up at the bottom of the page that contains its reference mark. This is the default value.
 // If we set the value of the "Position" property to "FootnotePosition.BeneathText",
 // every footnote will show up at the end of the page's text that contains its reference mark.
 doc.getFootnoteOptions().setPosition(footnotePosition);

 doc.save(getArtifactsDir() + "InlineStory.PositionFootnote.docx");
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [BENEATH_TEXT](#BENEATH-TEXT) | Le note a piè di pagina vengono generate sotto il testo in ogni pagina. |
| [BOTTOM_OF_PAGE](#BOTTOM-OF-PAGE) | Le note a piè di pagina vengono generate in fondo a ogni pagina. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String footnotePositionName)](#fromName-java.lang.String) |  |
| [getName(int footnotePosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int footnotePosition)](#toString-int) |  |
### BENEATH_TEXT {#BENEATH-TEXT}
```
public static int BENEATH_TEXT
```


Le note a piè di pagina vengono generate sotto il testo in ogni pagina.

### BOTTOM_OF_PAGE {#BOTTOM-OF-PAGE}
```
public static int BOTTOM_OF_PAGE
```


Le note a piè di pagina vengono generate in fondo a ogni pagina.

### length {#length}
```
public static int length
```


### fromName(String footnotePositionName) {#fromName-java.lang.String}
```
public static int fromName(String footnotePositionName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| footnotePositionName | java.lang.String |  |

**Returns:**
int
### getName(int footnotePosition) {#getName-int}
```
public static String getName(int footnotePosition)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| footnotePosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int footnotePosition) {#toString-int}
```
public static String toString(int footnotePosition)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| footnotePosition | int |  |

**Returns:**
java.lang.String
