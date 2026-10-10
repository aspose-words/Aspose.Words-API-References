---
title: "RelativeVerticalSize"
linktitle: "RelativeVerticalSize"
second_title: "Aspose.Words für Java"
description: "Gibt an, relativ zu welchem Bezug die Höhe einer Form oder eines Textframes in Java vertikal berechnet wird."
type: docs
weight: 564
url: /de/java/com.aspose.words/relativeverticalsize/
---

**Inheritance:**
java.lang.Object
```
public class RelativeVerticalSize
```

Gibt relativ an, worauf die Höhe einer Form oder eines Textfelds vertikal berechnet wird.

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
| [BOTTOM_MARGIN](#BOTTOM-MARGIN) | Gibt an, dass die Höhe relativ zur Größe des unteren Randbereichs berechnet wird. |
| [DEFAULT](#DEFAULT) | Standardwert ist [MARGIN](../../com.aspose.words/relativeverticalsize/\#MARGIN). |
| [INNER_MARGIN](#INNER-MARGIN) | Gibt an, dass die Höhe relativ zur Größe des Innenrandbereichs, zur Größe des oberen Randbereichs für ungerade Seiten und zur Größe des unteren Randbereichs für gerade Seiten berechnet wird. |
| [MARGIN](#MARGIN) | Gibt an, dass die Höhe relativ zum Abstand zwischen dem oberen und dem unteren Rand berechnet wird. |
| [OUTER_MARGIN](#OUTER-MARGIN) | Gibt an, dass die Höhe relativ zur Größe des Außenrandbereichs, zur Größe des unteren Randbereichs für ungerade Seiten und zur Größe des oberen Randbereichs für gerade Seiten berechnet wird. |
| [PAGE](#PAGE) | Gibt an, dass die Höhe relativ zur Seitenhöhe berechnet wird. |
| [TOP_MARGIN](#TOP-MARGIN) | Gibt an, dass die Höhe relativ zur Größe des oberen Randbereichs berechnet wird. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String relativeVerticalSizeName)](#fromName-java.lang.String) |  |
| [getName(int relativeVerticalSize)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeVerticalSize)](#toString-int) |  |
### BOTTOM_MARGIN {#BOTTOM-MARGIN}
```
public static int BOTTOM_MARGIN
```


Gibt an, dass die Höhe relativ zur Größe des unteren Randbereichs berechnet wird.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Standardwert ist [MARGIN](../../com.aspose.words/relativeverticalsize/\#MARGIN).

### INNER_MARGIN {#INNER-MARGIN}
```
public static int INNER_MARGIN
```


Gibt an, dass die Höhe relativ zur Größe des Innenrandbereichs, zur Größe des oberen Randbereichs für ungerade Seiten und zur Größe des unteren Randbereichs für gerade Seiten berechnet wird.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Gibt an, dass die Höhe relativ zum Abstand zwischen dem oberen und dem unteren Rand berechnet wird.

### OUTER_MARGIN {#OUTER-MARGIN}
```
public static int OUTER_MARGIN
```


Gibt an, dass die Höhe relativ zur Größe des Außenrandbereichs, zur Größe des unteren Randbereichs für ungerade Seiten und zur Größe des oberen Randbereichs für gerade Seiten berechnet wird.

### PAGE {#PAGE}
```
public static int PAGE
```


Gibt an, dass die Höhe relativ zur Seitenhöhe berechnet wird.

### TOP_MARGIN {#TOP-MARGIN}
```
public static int TOP_MARGIN
```


Gibt an, dass die Höhe relativ zur Größe des oberen Randbereichs berechnet wird.

### length {#length}
```
public static int length
```


### fromName(String relativeVerticalSizeName) {#fromName-java.lang.String}
```
public static int fromName(String relativeVerticalSizeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relativeVerticalSizeName | java.lang.String |  |

**Returns:**
int
### getName(int relativeVerticalSize) {#getName-int}
```
public static String getName(int relativeVerticalSize)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relativeVerticalSize | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeVerticalSize) {#toString-int}
```
public static String toString(int relativeVerticalSize)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relativeVerticalSize | int |  |

**Returns:**
java.lang.String
