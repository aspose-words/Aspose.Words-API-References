---
title: "CommentDisplayMode"
linktitle: "CommentDisplayMode"
second_title: "Aspose.Words für Java"
description: "Gibt den Rendermodus für Dokumentkommentare in Java an."
type: docs
weight: 110
url: /de/java/com.aspose.words/commentdisplaymode/
---

**Inheritance:**
java.lang.Object
```
public class CommentDisplayMode
```

Gibt den Rendermodus für Dokumentkommentare an.

 **Examples:** 

Zeigt, wie Kommentare beim Speichern eines Dokuments in ein gerendertes Format angezeigt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Hello world!");

 Comment comment = new Comment(doc, "John Doe", "J.D.", new Date());
 comment.setText("My comment.");
 builder.getCurrentParagraph().appendChild(comment);

 // ShowInAnnotations is only available in Pdf1.7 and Pdf1.5 formats.
 // In other formats, it will work similarly to Hide.
 doc.getLayoutOptions().setCommentDisplayMode(CommentDisplayMode.SHOW_IN_ANNOTATIONS);

 doc.save(getArtifactsDir() + "Document.ShowCommentsInAnnotations.pdf");

 // Note that it's required to rebuild the document page layout (via Document.UpdatePageLayout() method)
 // after changing the Document.LayoutOptions values.
 doc.getLayoutOptions().setCommentDisplayMode(CommentDisplayMode.SHOW_IN_BALLOONS);
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Document.ShowCommentsInBalloons.pdf");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [HIDE](#HIDE) | Keine Dokumentkommentare werden gerendert. |
| [SHOW_IN_ANNOTATIONS](#SHOW-IN-ANNOTATIONS) | Rendert Dokumentkommentare als Anmerkungen. |
| [SHOW_IN_BALLOONS](#SHOW-IN-BALLOONS) | Rendert Dokumentkommentare in Ballons im Rand. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String commentDisplayModeName)](#fromName-java.lang.String) |  |
| [getName(int commentDisplayMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int commentDisplayMode)](#toString-int) |  |
### HIDE {#HIDE}
```
public static int HIDE
```


Keine Dokumentkommentare werden gerendert.

### SHOW_IN_ANNOTATIONS {#SHOW-IN-ANNOTATIONS}
```
public static int SHOW_IN_ANNOTATIONS
```


Rendert Dokumentkommentare als Anmerkungen. Dies ist nur für das PDF‑Format verfügbar.

### SHOW_IN_BALLOONS {#SHOW-IN-BALLOONS}
```
public static int SHOW_IN_BALLOONS
```


Rendert Dokumentkommentare in Ballons im Rand. Dies ist der Standardwert.

### length {#length}
```
public static int length
```


### fromName(String commentDisplayModeName) {#fromName-java.lang.String}
```
public static int fromName(String commentDisplayModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| commentDisplayModeName | java.lang.String |  |

**Returns:**
int
### getName(int commentDisplayMode) {#getName-int}
```
public static String getName(int commentDisplayMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| commentDisplayMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int commentDisplayMode) {#toString-int}
```
public static String toString(int commentDisplayMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| commentDisplayMode | int |  |

**Returns:**
java.lang.String
