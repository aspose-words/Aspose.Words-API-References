---
title: ShapeLineStyle
linktitle: ShapeLineStyle
second_title: Aspose.Words for Java
description: Specifies the compound line style of a Shape in Java.
type: docs
weight: 552
url: /java/com.aspose.words/shapelinestyle/
---

**Inheritance:**
java.lang.Object
```
public class ShapeLineStyle
```

Specifies the compound line style of a [Shape](../../com.aspose.words/shape/).

 **Examples:** 

Shows how change stroke properties.

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
## Fields

| Field | Description |
| --- | --- |
| [DEFAULT](#DEFAULT) | Default value is [SINGLE](../../com.aspose.words/shapelinestyle/\#SINGLE). |
| [DOUBLE](#DOUBLE) | Double lines of equal width. |
| [SINGLE](#SINGLE) | Single line. |
| [THICK_THIN](#THICK-THIN) | Double lines, one thick, one thin. |
| [THIN_THICK](#THIN-THICK) | Double lines, one thin, one thick. |
| [TRIPLE](#TRIPLE) | Three lines, thin, thick, thin. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String shapeLineStyleName)](#fromName-java.lang.String) |  |
| [getName(int shapeLineStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeLineStyle)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Default value is [SINGLE](../../com.aspose.words/shapelinestyle/\#SINGLE).

### DOUBLE {#DOUBLE}
```
public static int DOUBLE
```


Double lines of equal width.

### SINGLE {#SINGLE}
```
public static int SINGLE
```


Single line.

### THICK_THIN {#THICK-THIN}
```
public static int THICK_THIN
```


Double lines, one thick, one thin.

### THIN_THICK {#THIN-THICK}
```
public static int THIN_THICK
```


Double lines, one thin, one thick.

### TRIPLE {#TRIPLE}
```
public static int TRIPLE
```


Three lines, thin, thick, thin.

### length {#length}
```
public static int length
```


### fromName(String shapeLineStyleName) {#fromName-java.lang.String}
```
public static int fromName(String shapeLineStyleName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| shapeLineStyleName | java.lang.String |  |

**Returns:**
int
### getName(int shapeLineStyle) {#getName-int}
```
public static String getName(int shapeLineStyle)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| shapeLineStyle | int |  |

**Returns:**
java.lang.String
