---
title: "ViewType"
linktitle: "ViewType"
second_title: "Aspose.Words für Java"
description: "Mögliche Werte für den Ansichtsmodus in Microsoft Word in Java."
type: docs
weight: 715
url: /de/java/com.aspose.words/viewtype/
---

**Inheritance:**
java.lang.Object
```
public class ViewType
```

Mögliche Werte für den Ansichtsmodus in Microsoft Word.

 **Examples:** 

Zeigt, wie ein benutzerdefinierter Zoomfaktor festgelegt wird, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [NONE](#NONE) | Das Dokument wird in der Standardansicht der Anwendung dargestellt. |
| [NORMAL](#NORMAL) | Das Dokument wird in einer Ansicht dargestellt, die für Gliederungen oder das Erstellen langer Dokumente optimiert ist. |
| [OUTLINE](#OUTLINE) | Das Dokument wird in einer Ansicht dargestellt, die für Gliederungen oder das Erstellen langer Dokumente optimiert ist. |
| [PAGE_LAYOUT](#PAGE-LAYOUT) | Das Dokument wird in einer Ansicht geöffnet, die das Dokument so anzeigt, wie es gedruckt wird. |
| [READING](#READING) | Das Dokument wird in der Standardansicht der Anwendung dargestellt. |
| [WEB](#WEB) | Das Dokument wird in einer Ansicht dargestellt, die nachahmt, wie dieses Dokument in einer Webseite angezeigt würde. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String viewTypeName)](#fromName-java.lang.String) |  |
| [getName(int viewType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int viewType)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Das Dokument wird in der Standardansicht der Anwendung dargestellt.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Das Dokument wird in einer Ansicht dargestellt, die für Gliederungen oder das Erstellen langer Dokumente optimiert ist.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


Das Dokument wird in einer Ansicht dargestellt, die für Gliederungen oder das Erstellen langer Dokumente optimiert ist.

### PAGE_LAYOUT {#PAGE-LAYOUT}
```
public static int PAGE_LAYOUT
```


Das Dokument wird in einer Ansicht geöffnet, die das Dokument so anzeigt, wie es gedruckt wird.

### READING {#READING}
```
public static int READING
```


Das Dokument wird in der Standardansicht der Anwendung dargestellt.

### WEB {#WEB}
```
public static int WEB
```


Das Dokument wird in einer Ansicht dargestellt, die nachahmt, wie dieses Dokument in einer Webseite angezeigt würde.

### length {#length}
```
public static int length
```


### fromName(String viewTypeName) {#fromName-java.lang.String}
```
public static int fromName(String viewTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| viewTypeName | java.lang.String |  |

**Returns:**
int
### getName(int viewType) {#getName-int}
```
public static String getName(int viewType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| viewType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int viewType) {#toString-int}
```
public static String toString(int viewType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| viewType | int |  |

**Returns:**
java.lang.String
