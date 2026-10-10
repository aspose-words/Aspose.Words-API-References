---
title: "ShapeLineStyle"
linktitle: "ShapeLineStyle"
second_title: "Aspose.Words per Java"
description: "Specifica lo stile di linea composto di una Shape in Java."
type: docs
weight: 614
url: /it/java/com.aspose.words/shapelinestyle/
---

**Inheritance:**
java.lang.Object
```
public class ShapeLineStyle
```

Specifica lo stile di linea composto di una [Shape](../../com.aspose.words/shape/).

 **Examples:** 

Mostra come modificare le proprietà del tratto.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [DEFAULT](#DEFAULT) | Il valore predefinito è [SINGLE](../../com.aspose.words/shapelinestyle/\#SINGLE). |
| [DOUBLE](#DOUBLE) | Linee doppie di larghezza uguale. |
| [SINGLE](#SINGLE) | Linea singola. |
| [THICK_THIN](#THICK-THIN) | Linee doppie, una spessa, una sottile. |
| [THIN_THICK](#THIN-THICK) | Linee doppie, una sottile, una spessa. |
| [TRIPLE](#TRIPLE) | Tre linee, sottile, spessa, sottile. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String shapeLineStyleName)](#fromName-java.lang.String) |  |
| [getName(int shapeLineStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeLineStyle)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Il valore predefinito è [SINGLE](../../com.aspose.words/shapelinestyle/\#SINGLE).

### DOUBLE {#DOUBLE}
```
public static int DOUBLE
```


Linee doppie di larghezza uguale.

### SINGLE {#SINGLE}
```
public static int SINGLE
```


Linea singola.

### THICK_THIN {#THICK-THIN}
```
public static int THICK_THIN
```


Linee doppie, una spessa, una sottile.

### THIN_THICK {#THIN-THICK}
```
public static int THIN_THICK
```


Linee doppie, una sottile, una spessa.

### TRIPLE {#TRIPLE}
```
public static int TRIPLE
```


Tre linee, sottile, spessa, sottile.

### length {#length}
```
public static int length
```


### fromName(String shapeLineStyleName) {#fromName-java.lang.String}
```
public static int fromName(String shapeLineStyleName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| shapeLineStyleName | java.lang.String |  |

**Returns:**
int
### getName(int shapeLineStyle) {#getName-int}
```
public static String getName(int shapeLineStyle)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| shapeLineStyle | int |  |

**Returns:**
java.lang.String
