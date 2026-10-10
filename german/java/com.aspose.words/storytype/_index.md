---
title: "StoryType"
linktitle: "StoryType"
second_title: "Aspose.Words für Java"
description: "Der Text eines Word-Dokuments wird in Java in Stories gespeichert."
type: docs
weight: 634
url: /de/java/com.aspose.words/storytype/
---

**Inheritance:**
java.lang.Object
```
public class StoryType
```

Der Text eines Word-Dokuments wird in Stories gespeichert. [StoryType](../../com.aspose.words/storytype/) identifiziert eine Story.

 **Examples:** 

Zeigt, wie alle Formen aus einem Knoten entfernt werden.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [COMMENTS](#COMMENTS) | Enthält Dokumentkommentare (Anmerkungen), dargestellt durch [Comment](../../com.aspose.words/comment/). |
| [ENDNOTES](#ENDNOTES) | Enthält Endnoten-Text, dargestellt durch [Footnote](../../com.aspose.words/footnote/). |
| [ENDNOTE_CONTINUATION_NOTICE](#ENDNOTE-CONTINUATION-NOTICE) | Enthält den Text des Trennzeichens für die Fortsetzungsmitteilung der Endnote. |
| [ENDNOTE_CONTINUATION_SEPARATOR](#ENDNOTE-CONTINUATION-SEPARATOR) | Enthält den Text des Endnoten‑Fortsetzungs‑Trennzeichens. |
| [ENDNOTE_SEPARATOR](#ENDNOTE-SEPARATOR) | Enthält den Text des Endnoten‑Trennzeichens. |
| [EVEN_PAGES_FOOTER](#EVEN-PAGES-FOOTER) | Enthält den Text der Fußzeile für gerade Seiten, dargestellt durch [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [EVEN_PAGES_HEADER](#EVEN-PAGES-HEADER) | Enthält den Text der Kopfzeile für gerade Seiten, dargestellt durch [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FIRST_PAGE_FOOTER](#FIRST-PAGE-FOOTER) | Enthält den Text der Fußzeile der ersten Seite, dargestellt durch [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FIRST_PAGE_HEADER](#FIRST-PAGE-HEADER) | Enthält den Text der Kopfzeile der ersten Seite, dargestellt durch [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FOOTNOTES](#FOOTNOTES) | Enthält den Text der Fußnote, dargestellt durch [Footnote](../../com.aspose.words/footnote/). |
| [FOOTNOTE_CONTINUATION_NOTICE](#FOOTNOTE-CONTINUATION-NOTICE) | Enthält den Text des Trennzeichens für den Fortsetzungs‑Hinweis der Fußnote. |
| [FOOTNOTE_CONTINUATION_SEPARATOR](#FOOTNOTE-CONTINUATION-SEPARATOR) | Enthält den Text des Trennzeichens für die Fortsetzung der Fußnote. |
| [FOOTNOTE_SEPARATOR](#FOOTNOTE-SEPARATOR) | Enthält den Text des Fußnoten‑Trennzeichens. |
| [MAIN_TEXT](#MAIN-TEXT) | Enthält den Haupttext des Dokuments, dargestellt durch [Body](../../com.aspose.words/body/). |
| [NONE](#NONE) | Standardwert. |
| [PRIMARY_FOOTER](#PRIMARY-FOOTER) | Enthält den Text der primären Fußzeile. |
| [PRIMARY_HEADER](#PRIMARY-HEADER) | Enthält den Text der primären Kopfzeile. |
| [TEXTBOX](#TEXTBOX) | Enthält Text von Form oder Textfeld, dargestellt durch [Shape](../../com.aspose.words/shape/). |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String storyTypeName)](#fromName-java.lang.String) |  |
| [getName(int storyType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int storyType)](#toString-int) |  |
### COMMENTS {#COMMENTS}
```
public static int COMMENTS
```


Enthält Dokumentkommentare (Anmerkungen), dargestellt durch [Comment](../../com.aspose.words/comment/).

### ENDNOTES {#ENDNOTES}
```
public static int ENDNOTES
```


Enthält Endnoten-Text, dargestellt durch [Footnote](../../com.aspose.words/footnote/).

### ENDNOTE_CONTINUATION_NOTICE {#ENDNOTE-CONTINUATION-NOTICE}
```
public static int ENDNOTE_CONTINUATION_NOTICE
```


Enthält den Text des Trennzeichens für die Fortsetzungsmitteilung der Endnote.

### ENDNOTE_CONTINUATION_SEPARATOR {#ENDNOTE-CONTINUATION-SEPARATOR}
```
public static int ENDNOTE_CONTINUATION_SEPARATOR
```


Enthält den Text des Endnoten‑Fortsetzungs‑Trennzeichens.

### ENDNOTE_SEPARATOR {#ENDNOTE-SEPARATOR}
```
public static int ENDNOTE_SEPARATOR
```


Enthält den Text des Endnoten‑Trennzeichens.

### EVEN_PAGES_FOOTER {#EVEN-PAGES-FOOTER}
```
public static int EVEN_PAGES_FOOTER
```


Enthält den Text der Fußzeile für gerade Seiten, dargestellt durch [HeaderFooter](../../com.aspose.words/headerfooter/).

### EVEN_PAGES_HEADER {#EVEN-PAGES-HEADER}
```
public static int EVEN_PAGES_HEADER
```


Enthält den Text der Kopfzeile für gerade Seiten, dargestellt durch [HeaderFooter](../../com.aspose.words/headerfooter/).

### FIRST_PAGE_FOOTER {#FIRST-PAGE-FOOTER}
```
public static int FIRST_PAGE_FOOTER
```


Enthält den Text der Fußzeile der ersten Seite, dargestellt durch [HeaderFooter](../../com.aspose.words/headerfooter/).

### FIRST_PAGE_HEADER {#FIRST-PAGE-HEADER}
```
public static int FIRST_PAGE_HEADER
```


Enthält den Text der Kopfzeile der ersten Seite, dargestellt durch [HeaderFooter](../../com.aspose.words/headerfooter/).

### FOOTNOTES {#FOOTNOTES}
```
public static int FOOTNOTES
```


Enthält den Text der Fußnote, dargestellt durch [Footnote](../../com.aspose.words/footnote/).

### FOOTNOTE_CONTINUATION_NOTICE {#FOOTNOTE-CONTINUATION-NOTICE}
```
public static int FOOTNOTE_CONTINUATION_NOTICE
```


Enthält den Text des Trennzeichens für den Fortsetzungs‑Hinweis der Fußnote.

### FOOTNOTE_CONTINUATION_SEPARATOR {#FOOTNOTE-CONTINUATION-SEPARATOR}
```
public static int FOOTNOTE_CONTINUATION_SEPARATOR
```


Enthält den Text des Trennzeichens für die Fortsetzung der Fußnote.

### FOOTNOTE_SEPARATOR {#FOOTNOTE-SEPARATOR}
```
public static int FOOTNOTE_SEPARATOR
```


Enthält den Text des Fußnoten‑Trennzeichens.

### MAIN_TEXT {#MAIN-TEXT}
```
public static int MAIN_TEXT
```


Enthält den Haupttext des Dokuments, dargestellt durch [Body](../../com.aspose.words/body/).

### NONE {#NONE}
```
public static int NONE
```


Standardwert. Es gibt keine solche Story im Dokument.

### PRIMARY_FOOTER {#PRIMARY-FOOTER}
```
public static int PRIMARY_FOOTER
```


Enthält den Text der primären Fußzeile. Wenn die Fußzeile für ungerade und gerade Seiten unterschiedlich ist, enthält sie den Text der Fußzeile für ungerade Seiten. Dargestellt durch [HeaderFooter](../../com.aspose.words/headerfooter/).

### PRIMARY_HEADER {#PRIMARY-HEADER}
```
public static int PRIMARY_HEADER
```


Enthält den Text der primären Kopfzeile. Wenn die Kopfzeile für ungerade und gerade Seiten unterschiedlich ist, enthält sie den Text der Kopfzeile für ungerade Seiten. Dargestellt durch [HeaderFooter](../../com.aspose.words/headerfooter/).

### TEXTBOX {#TEXTBOX}
```
public static int TEXTBOX
```


Enthält Text von Form oder Textfeld, dargestellt durch [Shape](../../com.aspose.words/shape/).

### length {#length}
```
public static int length
```


### fromName(String storyTypeName) {#fromName-java.lang.String}
```
public static int fromName(String storyTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| storyTypeName | java.lang.String |  |

**Returns:**
int
### getName(int storyType) {#getName-int}
```
public static String getName(int storyType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| storyType | int |  |

**Returns:**
java.lang.String
