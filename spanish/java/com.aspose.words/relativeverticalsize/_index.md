---
title: "RelativeVerticalSize"
linktitle: "RelativeVerticalSize"
second_title: "Aspose.Words para Java"
description: "Especifica respecto a qué se calcula verticalmente la altura de una forma o un marco de texto en Java."
type: docs
weight: 564
url: /es/java/com.aspose.words/relativeverticalsize/
---

**Inheritance:**
java.lang.Object
```
public class RelativeVerticalSize
```

Especifica respecto a qué se calcula verticalmente la altura de una forma o un marco de texto.

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
| [BOTTOM_MARGIN](#BOTTOM-MARGIN) | Especifica que la altura se calcula en relación al tamaño del área del margen inferior. |
| [DEFAULT](#DEFAULT) | El valor predeterminado es [MARGIN](../../com.aspose.words/relativeverticalsize/\#MARGIN). |
| [INNER_MARGIN](#INNER-MARGIN) | Especifica que la altura se calcula en relación al tamaño del área del margen interior, al tamaño del área del margen superior para páginas impares y al tamaño del área del margen inferior para páginas pares. |
| [MARGIN](#MARGIN) | Especifica que la altura se calcula en relación al espacio entre los márgenes superior e inferior. |
| [OUTER_MARGIN](#OUTER-MARGIN) | Especifica que la altura se calcula en relación al tamaño del área del margen exterior, al tamaño del área del margen inferior para páginas impares y al tamaño del área del margen superior para páginas pares. |
| [PAGE](#PAGE) | Especifica que la altura se calcula en relación a la altura de la página. |
| [TOP_MARGIN](#TOP-MARGIN) | Especifica que la altura se calcula en relación al tamaño del área del margen superior. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String relativeVerticalSizeName)](#fromName-java.lang.String) |  |
| [getName(int relativeVerticalSize)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeVerticalSize)](#toString-int) |  |
### BOTTOM_MARGIN {#BOTTOM-MARGIN}
```
public static int BOTTOM_MARGIN
```


Especifica que la altura se calcula en relación al tamaño del área del margen inferior.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


El valor predeterminado es [MARGIN](../../com.aspose.words/relativeverticalsize/\#MARGIN).

### INNER_MARGIN {#INNER-MARGIN}
```
public static int INNER_MARGIN
```


Especifica que la altura se calcula en relación al tamaño del área del margen interior, al tamaño del área del margen superior para páginas impares y al tamaño del área del margen inferior para páginas pares.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Especifica que la altura se calcula en relación al espacio entre los márgenes superior e inferior.

### OUTER_MARGIN {#OUTER-MARGIN}
```
public static int OUTER_MARGIN
```


Especifica que la altura se calcula en relación al tamaño del área del margen exterior, al tamaño del área del margen inferior para páginas impares y al tamaño del área del margen superior para páginas pares.

### PAGE {#PAGE}
```
public static int PAGE
```


Especifica que la altura se calcula en relación a la altura de la página.

### TOP_MARGIN {#TOP-MARGIN}
```
public static int TOP_MARGIN
```


Especifica que la altura se calcula en relación al tamaño del área del margen superior.

### length {#length}
```
public static int length
```


### fromName(String relativeVerticalSizeName) {#fromName-java.lang.String}
```
public static int fromName(String relativeVerticalSizeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relativeVerticalSizeName | java.lang.String |  |

**Returns:**
int
### getName(int relativeVerticalSize) {#getName-int}
```
public static String getName(int relativeVerticalSize)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relativeVerticalSize | int |  |

**Returns:**
java.lang.String
