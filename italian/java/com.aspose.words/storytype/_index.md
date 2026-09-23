---
title: "StoryType"
linktitle: "StoryType"
second_title: "Aspose.Words per Java"
description: "Il testo di un documento Word è memorizzato nelle storie in Java."
type: docs
weight: 634
url: /it/java/com.aspose.words/storytype/
---

**Inheritance:**
java.lang.Object
```
public class StoryType
```

Il testo di un documento Word è memorizzato nelle storie. [StoryType](../../com.aspose.words/storytype/) identifica una storia.

 **Examples:** 

Mostra come rimuovere tutte le forme da un nodo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a DocumentBuilder to insert a shape. This is an inline shape,
 // which has a parent Paragraph, which is a child node of the first section's Body.
 builder.insertShape(ShapeType.CUBE, 100.0, 100.0);

 Assert.assertEquals(doc.getChildNodes(NodeType.SHAPE, true).getCount(), 1);

 // We can delete all shapes from the child paragraphs of this Body.
 Assert.assertEquals(doc.getFirstSection().getBody().getStoryType(), StoryType.MAIN_TEXT);
 doc.getFirstSection().getBody().deleteShapes();

 Assert.assertEquals(doc.getChildNodes(NodeType.SHAPE, true).getCount(), 0);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [COMMENTS](#COMMENTS) | Contiene i commenti del documento (annotazioni), rappresentati da [Comment](../../com.aspose.words/comment/). |
| [ENDNOTES](#ENDNOTES) | Contiene il testo delle note a piè di pagina, rappresentato da [Footnote](../../com.aspose.words/footnote/). |
| [ENDNOTE_CONTINUATION_NOTICE](#ENDNOTE-CONTINUATION-NOTICE) | Contiene il testo del separatore di avviso di continuazione della nota a piè di pagina. |
| [ENDNOTE_CONTINUATION_SEPARATOR](#ENDNOTE-CONTINUATION-SEPARATOR) | Contiene il testo del separatore di continuazione della nota a piè di pagina. |
| [ENDNOTE_SEPARATOR](#ENDNOTE-SEPARATOR) | Contiene il testo del separatore della nota finale. |
| [EVEN_PAGES_FOOTER](#EVEN-PAGES-FOOTER) | Contiene il testo del piè di pagina delle pagine pari, rappresentato da [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [EVEN_PAGES_HEADER](#EVEN-PAGES-HEADER) | Contiene il testo dell'intestazione delle pagine pari, rappresentato da [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FIRST_PAGE_FOOTER](#FIRST-PAGE-FOOTER) | Contiene il testo del piè di pagina della prima pagina, rappresentato da [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FIRST_PAGE_HEADER](#FIRST-PAGE-HEADER) | Contiene il testo dell'intestazione della prima pagina, rappresentato da [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FOOTNOTES](#FOOTNOTES) | Contiene il testo della nota a piè di pagina, rappresentato da [Footnote](../../com.aspose.words/footnote/). |
| [FOOTNOTE_CONTINUATION_NOTICE](#FOOTNOTE-CONTINUATION-NOTICE) | Contiene il testo del separatore dell'avviso di continuazione della nota a piè di pagina. |
| [FOOTNOTE_CONTINUATION_SEPARATOR](#FOOTNOTE-CONTINUATION-SEPARATOR) | Contiene il testo del separatore di continuazione della nota a piè di pagina. |
| [FOOTNOTE_SEPARATOR](#FOOTNOTE-SEPARATOR) | Contiene il testo del separatore della nota a piè di pagina. |
| [MAIN_TEXT](#MAIN-TEXT) | Contiene il testo principale del documento, rappresentato da [Body](../../com.aspose.words/body/). |
| [NONE](#NONE) | Valore predefinito. |
| [PRIMARY_FOOTER](#PRIMARY-FOOTER) | Contiene il testo del piè di pagina principale. |
| [PRIMARY_HEADER](#PRIMARY-HEADER) | Contiene il testo dell'intestazione principale. |
| [TEXTBOX](#TEXTBOX) | Contiene il testo di forma o casella di testo, rappresentato da [Shape](../../com.aspose.words/shape/). |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String storyTypeName)](#fromName-java.lang.String) |  |
| [getName(int storyType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int storyType)](#toString-int) |  |
### COMMENTS {#COMMENTS}
```
public static int COMMENTS
```


Contiene i commenti del documento (annotazioni), rappresentati da [Comment](../../com.aspose.words/comment/).

### ENDNOTES {#ENDNOTES}
```
public static int ENDNOTES
```


Contiene il testo delle note a piè di pagina, rappresentato da [Footnote](../../com.aspose.words/footnote/).

### ENDNOTE_CONTINUATION_NOTICE {#ENDNOTE-CONTINUATION-NOTICE}
```
public static int ENDNOTE_CONTINUATION_NOTICE
```


Contiene il testo del separatore di avviso di continuazione della nota a piè di pagina.

### ENDNOTE_CONTINUATION_SEPARATOR {#ENDNOTE-CONTINUATION-SEPARATOR}
```
public static int ENDNOTE_CONTINUATION_SEPARATOR
```


Contiene il testo del separatore di continuazione della nota a piè di pagina.

### ENDNOTE_SEPARATOR {#ENDNOTE-SEPARATOR}
```
public static int ENDNOTE_SEPARATOR
```


Contiene il testo del separatore della nota finale.

### EVEN_PAGES_FOOTER {#EVEN-PAGES-FOOTER}
```
public static int EVEN_PAGES_FOOTER
```


Contiene il testo del piè di pagina delle pagine pari, rappresentato da [HeaderFooter](../../com.aspose.words/headerfooter/).

### EVEN_PAGES_HEADER {#EVEN-PAGES-HEADER}
```
public static int EVEN_PAGES_HEADER
```


Contiene il testo dell'intestazione delle pagine pari, rappresentato da [HeaderFooter](../../com.aspose.words/headerfooter/).

### FIRST_PAGE_FOOTER {#FIRST-PAGE-FOOTER}
```
public static int FIRST_PAGE_FOOTER
```


Contiene il testo del piè di pagina della prima pagina, rappresentato da [HeaderFooter](../../com.aspose.words/headerfooter/).

### FIRST_PAGE_HEADER {#FIRST-PAGE-HEADER}
```
public static int FIRST_PAGE_HEADER
```


Contiene il testo dell'intestazione della prima pagina, rappresentato da [HeaderFooter](../../com.aspose.words/headerfooter/).

### FOOTNOTES {#FOOTNOTES}
```
public static int FOOTNOTES
```


Contiene il testo della nota a piè di pagina, rappresentato da [Footnote](../../com.aspose.words/footnote/).

### FOOTNOTE_CONTINUATION_NOTICE {#FOOTNOTE-CONTINUATION-NOTICE}
```
public static int FOOTNOTE_CONTINUATION_NOTICE
```


Contiene il testo del separatore dell'avviso di continuazione della nota a piè di pagina.

### FOOTNOTE_CONTINUATION_SEPARATOR {#FOOTNOTE-CONTINUATION-SEPARATOR}
```
public static int FOOTNOTE_CONTINUATION_SEPARATOR
```


Contiene il testo del separatore di continuazione della nota a piè di pagina.

### FOOTNOTE_SEPARATOR {#FOOTNOTE-SEPARATOR}
```
public static int FOOTNOTE_SEPARATOR
```


Contiene il testo del separatore della nota a piè di pagina.

### MAIN_TEXT {#MAIN-TEXT}
```
public static int MAIN_TEXT
```


Contiene il testo principale del documento, rappresentato da [Body](../../com.aspose.words/body/).

### NONE {#NONE}
```
public static int NONE
```


Valore predefinito. Non esiste tale storia nel documento.

### PRIMARY_FOOTER {#PRIMARY-FOOTER}
```
public static int PRIMARY_FOOTER
```


Contiene il testo del piè di pagina principale. Quando il piè di pagina è diverso per le pagine dispari e pari, contiene il testo del piè di pagina delle pagine dispari. Rappresentato da [HeaderFooter](../../com.aspose.words/headerfooter/).

### PRIMARY_HEADER {#PRIMARY-HEADER}
```
public static int PRIMARY_HEADER
```


Contiene il testo dell'intestazione principale. Quando l'intestazione è diversa per le pagine dispari e pari, contiene il testo dell'intestazione delle pagine dispari. Rappresentato da [HeaderFooter](../../com.aspose.words/headerfooter/).

### TEXTBOX {#TEXTBOX}
```
public static int TEXTBOX
```


Contiene il testo di forma o casella di testo, rappresentato da [Shape](../../com.aspose.words/shape/).

### length {#length}
```
public static int length
```


### fromName(String storyTypeName) {#fromName-java.lang.String}
```
public static int fromName(String storyTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| storyTypeName | java.lang.String |  |

**Returns:**
int
### getName(int storyType) {#getName-int}
```
public static String getName(int storyType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| storyType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int storyType) {#toString-int}
```
public static String toString(int storyType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| storyType | int |  |

**Returns:**
java.lang.String
