---
title: "ShapeLineStyle"
linktitle: "ShapeLineStyle"
second_title: "Aspose.Words für Java"
description: "Gibt den zusammengesetzten Linienstil eines Shape in Java an."
type: docs
weight: 614
url: /de/java/com.aspose.words/shapelinestyle/
---

**Inheritance:**
java.lang.Object
```
public class ShapeLineStyle
```

Gibt den zusammengesetzten Linienstil eines [Shape](../../com.aspose.words/shape/) an.

 **Examples:** 

Zeigt, wie Strich-Eigenschaften geändert werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 200.0, 200.0, WrapType.NONE);

 // Basic shapes, such as the rectangle, have two visible parts.
 // 1 -  The fill, which applies to the area within the outline of the shape:
 shape.getFill().setForeColor(Color.WHITE);

 // 2 -  The stroke, which marks the outline of the shape:
 // Modify various properties of this shape's stroke.
 Stroke stroke = shape.getStroke();
 stroke.setOn(true);
 stroke.setWeight(5.0);
 stroke.setColor(Color.RED);
 stroke.setDashStyle(DashStyle.SHORT_DASH_DOT_DOT);
 stroke.setJoinStyle(JoinStyle.MITER);
 stroke.setEndCap(EndCap.SQUARE);
 stroke.setLineStyle(ShapeLineStyle.TRIPLE);
 stroke.getFill().twoColorGradient(Color.RED, Color.BLUE, GradientStyle.VERTICAL, GradientVariant.VARIANT_1);

 doc.save(getArtifactsDir() + "Shape.Stroke.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [DEFAULT](#DEFAULT) | Standardwert ist [SINGLE](../../com.aspose.words/shapelinestyle/\#SINGLE). |
| [DOUBLE](#DOUBLE) | Doppelte Linien gleicher Breite. |
| [SINGLE](#SINGLE) | Einzelne Linie. |
| [THICK_THIN](#THICK-THIN) | Doppelte Linien, eine dick, eine dünn. |
| [THIN_THICK](#THIN-THICK) | Doppelte Linien, eine dünn, eine dick. |
| [TRIPLE](#TRIPLE) | Drei Linien, dünn, dick, dünn. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String shapeLineStyleName)](#fromName-java.lang.String) |  |
| [getName(int shapeLineStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeLineStyle)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Standardwert ist [SINGLE](../../com.aspose.words/shapelinestyle/\#SINGLE).

### DOUBLE {#DOUBLE}
```
public static int DOUBLE
```


Doppelte Linien gleicher Breite.

### SINGLE {#SINGLE}
```
public static int SINGLE
```


Einzelne Linie.

### THICK_THIN {#THICK-THIN}
```
public static int THICK_THIN
```


Doppelte Linien, eine dick, eine dünn.

### THIN_THICK {#THIN-THICK}
```
public static int THIN_THICK
```


Doppelte Linien, eine dünn, eine dick.

### TRIPLE {#TRIPLE}
```
public static int TRIPLE
```


Drei Linien, dünn, dick, dünn.

### length {#length}
```
public static int length
```


### fromName(String shapeLineStyleName) {#fromName-java.lang.String}
```
public static int fromName(String shapeLineStyleName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shapeLineStyleName | java.lang.String |  |

**Returns:**
int
### getName(int shapeLineStyle) {#getName-int}
```
public static String getName(int shapeLineStyle)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shapeLineStyle | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int shapeLineStyle) {#toString-int}
```
public static String toString(int shapeLineStyle)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shapeLineStyle | int |  |

**Returns:**
java.lang.String
