---
title: "FootnotePosition"
linktitle: "FootnotePosition"
second_title: "Aspose.Words pour Java"
description: "Définit la position de la note de bas de page en Java."
type: docs
weight: 342
url: /fr/java/com.aspose.words/footnoteposition/
---

**Inheritance:**
java.lang.Object
```
public class FootnotePosition
```

Définit la position de la note de bas de page.

 **Examples:** 

Montre comment sélectionner un emplacement différent où le document collecte et affiche ses notes de bas de page.

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
## Champs

| Champ | Description |
| --- | --- |
| [BENEATH_TEXT](#BENEATH-TEXT) | Les notes de bas de page sont affichées sous le texte sur chaque page. |
| [BOTTOM_OF_PAGE](#BOTTOM-OF-PAGE) | Les notes de bas de page sont affichées en bas de chaque page. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String footnotePositionName)](#fromName-java.lang.String) |  |
| [getName(int footnotePosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int footnotePosition)](#toString-int) |  |
### BENEATH_TEXT {#BENEATH-TEXT}
```
public static int BENEATH_TEXT
```


Les notes de bas de page sont affichées sous le texte sur chaque page.

### BOTTOM_OF_PAGE {#BOTTOM-OF-PAGE}
```
public static int BOTTOM_OF_PAGE
```


Les notes de bas de page sont affichées en bas de chaque page.

### length {#length}
```
public static int length
```


### fromName(String footnotePositionName) {#fromName-java.lang.String}
```
public static int fromName(String footnotePositionName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| footnotePositionName | java.lang.String |  |

**Returns:**
int
### getName(int footnotePosition) {#getName-int}
```
public static String getName(int footnotePosition)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| footnotePosition | int |  |

**Returns:**
java.lang.String
