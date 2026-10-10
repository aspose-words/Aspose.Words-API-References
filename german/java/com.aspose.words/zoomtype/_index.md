---
title: "ZoomType"
linktitle: "ZoomType"
second_title: "Aspose.Words für Java"
description: "Mögliche Werte dafür, wie groß oder klein das Dokument auf dem Bildschirm in Microsoft Word in Java angezeigt wird."
type: docs
weight: 751
url: /de/java/com.aspose.words/zoomtype/
---

**Inheritance:**
java.lang.Object
```
public class ZoomType
```

Mögliche Werte dafür, wie groß oder klein das Dokument in Microsoft Word auf dem Bildschirm angezeigt wird.

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
| [CUSTOM](#CUSTOM) | Der Zoom-Prozentsatz wird explizit festgelegt. |
| [FULL_PAGE](#FULL-PAGE) | Der Zoom-Prozentsatz wird automatisch neu berechnet, um eine ganze Seite anzupassen. |
| [NONE](#NONE) | Gibt an, den expliziten Zoom-Prozentsatz zu verwenden. |
| [PAGE_WIDTH](#PAGE-WIDTH) | Der Zoom-Prozentsatz wird automatisch neu berechnet, um die Seitenbreite anzupassen. |
| [TEXT_FIT](#TEXT-FIT) | Der Zoom-Prozentsatz wird automatisch neu berechnet, um den Text anzupassen. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String zoomTypeName)](#fromName-java.lang.String) |  |
| [getName(int zoomType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int zoomType)](#toString-int) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Der Zoom-Prozentsatz wird explizit festgelegt. Er wird nicht automatisch neu berechnet, wenn die Größe des Steuerelements geändert wird.

### FULL_PAGE {#FULL-PAGE}
```
public static int FULL_PAGE
```


Der Zoom-Prozentsatz wird automatisch neu berechnet, um eine ganze Seite anzupassen.

### NONE {#NONE}
```
public static int NONE
```


Gibt an, den expliziten Zoom-Prozentsatz zu verwenden. Gleich wie [CUSTOM](../../com.aspose.words/zoomtype/\#CUSTOM).

### PAGE_WIDTH {#PAGE-WIDTH}
```
public static int PAGE_WIDTH
```


Der Zoom-Prozentsatz wird automatisch neu berechnet, um die Seitenbreite anzupassen.

### TEXT_FIT {#TEXT-FIT}
```
public static int TEXT_FIT
```


Der Zoom-Prozentsatz wird automatisch neu berechnet, um den Text anzupassen.

### length {#length}
```
public static int length
```


### fromName(String zoomTypeName) {#fromName-java.lang.String}
```
public static int fromName(String zoomTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| zoomTypeName | java.lang.String |  |

**Returns:**
int
### getName(int zoomType) {#getName-int}
```
public static String getName(int zoomType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| zoomType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int zoomType) {#toString-int}
```
public static String toString(int zoomType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| zoomType | int |  |

**Returns:**
java.lang.String
