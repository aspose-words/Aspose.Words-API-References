---
title: "ShapeLineStyle"
linktitle: "ShapeLineStyle"
second_title: "Aspose.Words pour Java"
description: "Spécifie le style de ligne composé d'un Shape en Java."
type: docs
weight: 614
url: /fr/java/com.aspose.words/shapelinestyle/
---

**Inheritance:**
java.lang.Object
```
public class ShapeLineStyle
```

Spécifie le style de ligne composé d'un [Shape](../../com.aspose.words/shape/).

 **Examples:** 

Montre comment modifier les propriétés du trait.

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
## Champs

| Champ | Description |
| --- | --- |
| [DEFAULT](#DEFAULT) | La valeur par défaut est [SINGLE](../../com.aspose.words/shapelinestyle/\#SINGLE). |
| [DOUBLE](#DOUBLE) | Lignes doubles de largeur égale. |
| [SINGLE](#SINGLE) | Ligne simple. |
| [THICK_THIN](#THICK-THIN) | Lignes doubles, une épaisse, une fine. |
| [THIN_THICK](#THIN-THICK) | Lignes doubles, une fine, une épaisse. |
| [TRIPLE](#TRIPLE) | Trois lignes, fine, épaisse, fine. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String shapeLineStyleName)](#fromName-java.lang.String) |  |
| [getName(int shapeLineStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeLineStyle)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


La valeur par défaut est [SINGLE](../../com.aspose.words/shapelinestyle/\#SINGLE).

### DOUBLE {#DOUBLE}
```
public static int DOUBLE
```


Lignes doubles de largeur égale.

### SINGLE {#SINGLE}
```
public static int SINGLE
```


Ligne simple.

### THICK_THIN {#THICK-THIN}
```
public static int THICK_THIN
```


Lignes doubles, une épaisse, une fine.

### THIN_THICK {#THIN-THICK}
```
public static int THIN_THICK
```


Lignes doubles, une fine, une épaisse.

### TRIPLE {#TRIPLE}
```
public static int TRIPLE
```


Trois lignes, fine, épaisse, fine.

### length {#length}
```
public static int length
```


### fromName(String shapeLineStyleName) {#fromName-java.lang.String}
```
public static int fromName(String shapeLineStyleName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| shapeLineStyleName | java.lang.String |  |

**Returns:**
int
### getName(int shapeLineStyle) {#getName-int}
```
public static String getName(int shapeLineStyle)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| shapeLineStyle | int |  |

**Returns:**
java.lang.String
