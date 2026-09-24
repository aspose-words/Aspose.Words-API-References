---
title: "ShapeLineStyle"
linktitle: "ShapeLineStyle"
second_title: "Aspose.Words para Java"
description: "Especifica el estilo de línea compuesto de un Shape en Java."
type: docs
weight: 614
url: /es/java/com.aspose.words/shapelinestyle/
---

**Inheritance:**
java.lang.Object
```
public class ShapeLineStyle
```

Especifica el estilo de línea compuesto de un [Shape](../../com.aspose.words/shape/).

 **Examples:** 

Muestra cómo cambiar las propiedades del trazo.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [DEFAULT](#DEFAULT) | El valor predeterminado es [SINGLE](../../com.aspose.words/shapelinestyle/\#SINGLE). |
| [DOUBLE](#DOUBLE) | Líneas dobles de igual ancho. |
| [SINGLE](#SINGLE) | Línea simple. |
| [THICK_THIN](#THICK-THIN) | Líneas dobles, una gruesa y una delgada. |
| [THIN_THICK](#THIN-THICK) | Líneas dobles, una delgada y una gruesa. |
| [TRIPLE](#TRIPLE) | Tres líneas, delgada, gruesa, delgada. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String shapeLineStyleName)](#fromName-java.lang.String) |  |
| [getName(int shapeLineStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeLineStyle)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


El valor predeterminado es [SINGLE](../../com.aspose.words/shapelinestyle/\#SINGLE).

### DOUBLE {#DOUBLE}
```
public static int DOUBLE
```


Líneas dobles de igual ancho.

### SINGLE {#SINGLE}
```
public static int SINGLE
```


Línea simple.

### THICK_THIN {#THICK-THIN}
```
public static int THICK_THIN
```


Líneas dobles, una gruesa y una delgada.

### THIN_THICK {#THIN-THICK}
```
public static int THIN_THICK
```


Líneas dobles, una delgada y una gruesa.

### TRIPLE {#TRIPLE}
```
public static int TRIPLE
```


Tres líneas, delgada, gruesa, delgada.

### length {#length}
```
public static int length
```


### fromName(String shapeLineStyleName) {#fromName-java.lang.String}
```
public static int fromName(String shapeLineStyleName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| shapeLineStyleName | java.lang.String |  |

**Returns:**
int
### getName(int shapeLineStyle) {#getName-int}
```
public static String getName(int shapeLineStyle)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| shapeLineStyle | int |  |

**Returns:**
java.lang.String
