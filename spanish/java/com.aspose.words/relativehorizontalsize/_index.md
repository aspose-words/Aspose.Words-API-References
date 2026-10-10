---
title: "RelativeHorizontalSize"
linktitle: "RelativeHorizontalSize"
second_title: "Aspose.Words para Java"
description: "Especifica relativamente a qué se calcula horizontalmente el ancho de una forma o un marco de texto en Java."
type: docs
weight: 562
url: /es/java/com.aspose.words/relativehorizontalsize/
---

**Inheritance:**
java.lang.Object
```
public class RelativeHorizontalSize
```

Especifica respecto a qué se calcula horizontalmente el ancho de una forma o un marco de texto.

 **Examples:** 

Muestra cómo establecer el tamaño y la posición relativos.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [DEFAULT](#DEFAULT) | El valor predeterminado es [MARGIN](../../com.aspose.words/relativehorizontalsize/\#MARGIN). |
| [INNER_MARGIN](#INNER-MARGIN) | Especifica que el ancho se calcula relativamente al tamaño del área del margen interior, al tamaño del margen izquierdo para páginas impares y al tamaño del margen derecho para páginas pares. |
| [LEFT_MARGIN](#LEFT-MARGIN) | Especifica que el ancho se calcula relativamente al tamaño del margen izquierdo. |
| [MARGIN](#MARGIN) | Especifica que el ancho se calcula relativamente al espacio entre los márgenes izquierdo y derecho. |
| [OUTER_MARGIN](#OUTER-MARGIN) | Especifica que el ancho se calcula en relación al tamaño del área del margen exterior, al tamaño del área del margen derecho para páginas impares y al tamaño del área del margen izquierdo para páginas pares. |
| [PAGE](#PAGE) | Especifica que el ancho se calcula en relación al ancho de la página. |
| [RIGHT_MARGIN](#RIGHT-MARGIN) | Especifica que el ancho se calcula en relación al tamaño del área del margen derecho. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String relativeHorizontalSizeName)](#fromName-java.lang.String) |  |
| [getName(int relativeHorizontalSize)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeHorizontalSize)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


El valor predeterminado es [MARGIN](../../com.aspose.words/relativehorizontalsize/\#MARGIN).

### INNER_MARGIN {#INNER-MARGIN}
```
public static int INNER_MARGIN
```


Especifica que el ancho se calcula relativamente al tamaño del área del margen interior, al tamaño del margen izquierdo para páginas impares y al tamaño del margen derecho para páginas pares.

### LEFT_MARGIN {#LEFT-MARGIN}
```
public static int LEFT_MARGIN
```


Especifica que el ancho se calcula relativamente al tamaño del margen izquierdo.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Especifica que el ancho se calcula relativamente al espacio entre los márgenes izquierdo y derecho.

### OUTER_MARGIN {#OUTER-MARGIN}
```
public static int OUTER_MARGIN
```


Especifica que el ancho se calcula en relación al tamaño del área del margen exterior, al tamaño del área del margen derecho para páginas impares y al tamaño del área del margen izquierdo para páginas pares.

### PAGE {#PAGE}
```
public static int PAGE
```


Especifica que el ancho se calcula en relación al ancho de la página.

### RIGHT_MARGIN {#RIGHT-MARGIN}
```
public static int RIGHT_MARGIN
```


Especifica que el ancho se calcula en relación al tamaño del área del margen derecho.

### length {#length}
```
public static int length
```


### fromName(String relativeHorizontalSizeName) {#fromName-java.lang.String}
```
public static int fromName(String relativeHorizontalSizeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relativeHorizontalSizeName | java.lang.String |  |

**Returns:**
int
### getName(int relativeHorizontalSize) {#getName-int}
```
public static String getName(int relativeHorizontalSize)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relativeHorizontalSize | int |  |

**Returns:**
java.lang.String
