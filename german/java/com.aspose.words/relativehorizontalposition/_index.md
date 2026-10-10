---
title: "RelativeHorizontalPosition"
linktitle: "RelativeHorizontalPosition"
second_title: "Aspose.Words für Java"
description: "Gibt an, worauf sich die horizontale Position einer Form oder eines Textrahmens in Java bezieht."
type: docs
weight: 561
url: /de/java/com.aspose.words/relativehorizontalposition/
---

**Inheritance:**
java.lang.Object
```
public class RelativeHorizontalPosition
```

Gibt an, worauf sich die horizontale Position einer Form oder eines Textfelds bezieht.

 **Examples:** 

Zeigt, wie man ein Bild einfügt und es als Wasserzeichen verwendet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

Zeigt, wie man ein schwebendes Bild in die Mitte einer Seite einfügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CHARACTER](#CHARACTER) | Das Objekt ist relativ zur linken Seite des Absatzes positioniert. |
| [COLUMN](#COLUMN) | Das Objekt ist relativ zur linken Seite der Spalte positioniert. |
| [DEFAULT](#DEFAULT) | Standardwert ist [COLUMN](../../com.aspose.words/relativehorizontalposition/\#COLUMN). |
| [INSIDE_MARGIN](#INSIDE-MARGIN) | Gibt an, dass die horizontale Positionierung relativ zum Innenrand der aktuellen Seite sein soll (der linke Rand bei ungeraden Seiten, der rechte bei geraden Seiten). |
| [LEFT_MARGIN](#LEFT-MARGIN) | Gibt an, dass die horizontale Positionierung relativ zum linken Rand der Seite sein soll. |
| [MARGIN](#MARGIN) | Gibt an, dass die horizontale Positionierung relativ zu den Seitenrändern sein soll. |
| [OUTSIDE_MARGIN](#OUTSIDE-MARGIN) | Gibt an, dass die horizontale Positionierung relativ zum Außenrand der aktuellen Seite sein soll (der rechte Rand bei ungeraden Seiten, der linke bei geraden Seiten). |
| [PAGE](#PAGE) | Das Objekt ist relativ zur linken Kante der Seite positioniert. |
| [RIGHT_MARGIN](#RIGHT-MARGIN) | Gibt an, dass die horizontale Positionierung relativ zum rechten Rand der Seite sein soll. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String relativeHorizontalPositionName)](#fromName-java.lang.String) |  |
| [getName(int relativeHorizontalPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeHorizontalPosition)](#toString-int) |  |
### CHARACTER {#CHARACTER}
```
public static int CHARACTER
```


Das Objekt ist relativ zur linken Seite des Absatzes positioniert.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Das Objekt ist relativ zur linken Seite der Spalte positioniert.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Standardwert ist [COLUMN](../../com.aspose.words/relativehorizontalposition/\#COLUMN).

### INSIDE_MARGIN {#INSIDE-MARGIN}
```
public static int INSIDE_MARGIN
```


Gibt an, dass die horizontale Positionierung relativ zum Innenrand der aktuellen Seite sein soll (der linke Rand bei ungeraden Seiten, der rechte bei geraden Seiten).

### LEFT_MARGIN {#LEFT-MARGIN}
```
public static int LEFT_MARGIN
```


Gibt an, dass die horizontale Positionierung relativ zum linken Rand der Seite sein soll.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Gibt an, dass die horizontale Positionierung relativ zu den Seitenrändern sein soll.

### OUTSIDE_MARGIN {#OUTSIDE-MARGIN}
```
public static int OUTSIDE_MARGIN
```


Gibt an, dass die horizontale Positionierung relativ zum Außenrand der aktuellen Seite sein soll (der rechte Rand bei ungeraden Seiten, der linke bei geraden Seiten).

### PAGE {#PAGE}
```
public static int PAGE
```


Das Objekt ist relativ zur linken Kante der Seite positioniert.

### RIGHT_MARGIN {#RIGHT-MARGIN}
```
public static int RIGHT_MARGIN
```


Gibt an, dass die horizontale Positionierung relativ zum rechten Rand der Seite sein soll.

### length {#length}
```
public static int length
```


### fromName(String relativeHorizontalPositionName) {#fromName-java.lang.String}
```
public static int fromName(String relativeHorizontalPositionName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relativeHorizontalPositionName | java.lang.String |  |

**Returns:**
int
### getName(int relativeHorizontalPosition) {#getName-int}
```
public static String getName(int relativeHorizontalPosition)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relativeHorizontalPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeHorizontalPosition) {#toString-int}
```
public static String toString(int relativeHorizontalPosition)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relativeHorizontalPosition | int |  |

**Returns:**
java.lang.String
