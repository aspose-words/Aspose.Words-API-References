---
title: "RelativeHorizontalSize"
linktitle: "RelativeHorizontalSize"
second_title: "Aspose.Words für Java"
description: "Gibt relativ an, wovon die Breite einer Form oder eines Textrahmens horizontal in Java berechnet wird."
type: docs
weight: 562
url: /de/java/com.aspose.words/relativehorizontalsize/
---

**Inheritance:**
java.lang.Object
```
public class RelativeHorizontalSize
```

Gibt relativ an, worauf die Breite einer Form oder eines Textfelds horizontal berechnet wird.

 **Examples:** 

Zeigt, wie relative Größe und Position festgelegt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Adding a simple shape with absolute size and position.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 40.0);
 // Set WrapType to WrapType.None since Inline shapes are automatically converted to absolute units.
 shape.setWrapType(WrapType.NONE);

 // Checking and setting the relative horizontal size.
 if (shape.getRelativeHorizontalSize() == RelativeHorizontalSize.DEFAULT)
 {
     // Setting the horizontal size binding to Margin.
     shape.setRelativeHorizontalSize(RelativeHorizontalSize.MARGIN);
     // Setting the width to 50% of Margin width.
     shape.setWidthRelative(50f);
 }

 // Checking and setting the relative vertical size.
 if (shape.getRelativeVerticalSize() == RelativeVerticalSize.DEFAULT)
 {
     // Setting the vertical size binding to Margin.
     shape.setRelativeVerticalSize(RelativeVerticalSize.MARGIN);
     // Setting the heigh to 30% of Margin height.
     shape.setHeightRelative(30f);
 }

 // Checking and setting the relative vertical position.
 if (shape.getRelativeVerticalPosition() == RelativeVerticalPosition.PARAGRAPH)
 {
     // etting the position binding to TopMargin.
     shape.setRelativeVerticalPosition(RelativeVerticalPosition.TOP_MARGIN);
     // Setting relative Top to 30% of TopMargin position.
     shape.setTopRelative(30f);
 }

 // Checking and setting the relative horizontal position.
 if (shape.getRelativeHorizontalPosition() == RelativeHorizontalPosition.DEFAULT)
 {
     // Setting the position binding to RightMargin.
     shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.RIGHT_MARGIN);
     // The position relative value can be negative.
     shape.setLeftRelative(-260);
 }

 doc.save(getArtifactsDir() + "Shape.RelativeSizeAndPosition.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [DEFAULT](#DEFAULT) | Standardwert ist [MARGIN](../../com.aspose.words/relativehorizontalsize/\#MARGIN). |
| [INNER_MARGIN](#INNER-MARGIN) | Gibt an, dass die Breite relativ zur Größe des inneren Randbereichs, zur Größe des linken Randbereichs für ungerade Seiten und zur Größe des rechten Randbereichs für gerade Seiten berechnet wird. |
| [LEFT_MARGIN](#LEFT-MARGIN) | Gibt an, dass die Breite relativ zur Größe des linken Randbereichs berechnet wird. |
| [MARGIN](#MARGIN) | Gibt an, dass die Breite relativ zum Abstand zwischen dem linken und dem rechten Rand berechnet wird. |
| [OUTER_MARGIN](#OUTER-MARGIN) | Gibt an, dass die Breite relativ zur Größe des äußeren Randbereichs, zur Größe des rechten Randbereichs für ungerade Seiten und zur Größe des linken Randbereichs für gerade Seiten berechnet wird. |
| [PAGE](#PAGE) | Gibt an, dass die Breite relativ zur Seitenbreite berechnet wird. |
| [RIGHT_MARGIN](#RIGHT-MARGIN) | Gibt an, dass die Breite relativ zur Größe des rechten Randbereichs berechnet wird. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String relativeHorizontalSizeName)](#fromName-java.lang.String) |  |
| [getName(int relativeHorizontalSize)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeHorizontalSize)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Standardwert ist [MARGIN](../../com.aspose.words/relativehorizontalsize/\#MARGIN).

### INNER_MARGIN {#INNER-MARGIN}
```
public static int INNER_MARGIN
```


Gibt an, dass die Breite relativ zur Größe des inneren Randbereichs, zur Größe des linken Randbereichs für ungerade Seiten und zur Größe des rechten Randbereichs für gerade Seiten berechnet wird.

### LEFT_MARGIN {#LEFT-MARGIN}
```
public static int LEFT_MARGIN
```


Gibt an, dass die Breite relativ zur Größe des linken Randbereichs berechnet wird.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Gibt an, dass die Breite relativ zum Abstand zwischen dem linken und dem rechten Rand berechnet wird.

### OUTER_MARGIN {#OUTER-MARGIN}
```
public static int OUTER_MARGIN
```


Gibt an, dass die Breite relativ zur Größe des äußeren Randbereichs, zur Größe des rechten Randbereichs für ungerade Seiten und zur Größe des linken Randbereichs für gerade Seiten berechnet wird.

### PAGE {#PAGE}
```
public static int PAGE
```


Gibt an, dass die Breite relativ zur Seitenbreite berechnet wird.

### RIGHT_MARGIN {#RIGHT-MARGIN}
```
public static int RIGHT_MARGIN
```


Gibt an, dass die Breite relativ zur Größe des rechten Randbereichs berechnet wird.

### length {#length}
```
public static int length
```


### fromName(String relativeHorizontalSizeName) {#fromName-java.lang.String}
```
public static int fromName(String relativeHorizontalSizeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relativeHorizontalSizeName | java.lang.String |  |

**Returns:**
int
### getName(int relativeHorizontalSize) {#getName-int}
```
public static String getName(int relativeHorizontalSize)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relativeHorizontalSize | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeHorizontalSize) {#toString-int}
```
public static String toString(int relativeHorizontalSize)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relativeHorizontalSize | int |  |

**Returns:**
java.lang.String
