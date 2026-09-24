---
title: "BorderType"
linktitle: "BorderType"
second_title: "Aspose.Words para Java"
description: "Especifica los lados de un borde en Java."
type: docs
weight: 48
url: /es/java/com.aspose.words/bordertype/
---

**Inheritance:**
java.lang.Object
```
public class BorderType
```

Especifica los lados de un borde.

Para obtener más información, visite el artículo de documentación [ Programming with Documents ][Programming with Documents].

 **Examples:** 

Muestra cómo insertar un párrafo con un borde superior.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Border topBorder = builder.getParagraphFormat().getBorders().getByBorderType(BorderType.TOP);
 topBorder.setLineWidth(4.0d);
 topBorder.setLineStyle(LineStyle.DASH_SMALL_GAP);
 // Set ThemeColor only when LineWidth or LineStyle setted.
 topBorder.setThemeColor(ThemeColor.ACCENT_1);
 topBorder.setTintAndShade(0.25d);

 builder.writeln("Text with a top border.");

 doc.save(getArtifactsDir() + "Border.ParagraphTopBorder.docx");
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Campos

| Campo | Descripción |
| --- | --- |
| [BOTTOM](#BOTTOM) | Especifica el borde inferior de un párrafo o una celda de tabla. |
| [DIAGONAL_DOWN](#DIAGONAL-DOWN) | Especifica el borde diagonal en una celda de tabla. |
| [DIAGONAL_UP](#DIAGONAL-UP) | Especifica el borde diagonal en una celda de tabla. |
| [HORIZONTAL](#HORIZONTAL) | Especifica el borde horizontal entre celdas en una tabla o entre párrafos conformes. |
| [LEFT](#LEFT) | Especifica el borde izquierdo de un párrafo o una celda de tabla. |
| [NONE](#NONE) | Valor predeterminado. |
| [RIGHT](#RIGHT) | Especifica el borde derecho de un párrafo o una celda de tabla. |
| [TOP](#TOP) | Especifica el borde superior de un párrafo o una celda de tabla. |
| [VERTICAL](#VERTICAL) | Especifica el borde vertical entre celdas en una tabla. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String borderTypeName)](#fromName-java.lang.String) |  |
| [getName(int borderType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int borderType)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Especifica el borde inferior de un párrafo o una celda de tabla.

### DIAGONAL_DOWN {#DIAGONAL-DOWN}
```
public static int DIAGONAL_DOWN
```


Especifica el borde diagonal en una celda de tabla.

### DIAGONAL_UP {#DIAGONAL-UP}
```
public static int DIAGONAL_UP
```


Especifica el borde diagonal en una celda de tabla.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Especifica el borde horizontal entre celdas en una tabla o entre párrafos conformes.

### LEFT {#LEFT}
```
public static int LEFT
```


Especifica el borde izquierdo de un párrafo o una celda de tabla.

### NONE {#NONE}
```
public static int NONE
```


Valor predeterminado.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Especifica el borde derecho de un párrafo o una celda de tabla.

### TOP {#TOP}
```
public static int TOP
```


Especifica el borde superior de un párrafo o una celda de tabla.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Especifica el borde vertical entre celdas en una tabla.

### length {#length}
```
public static int length
```


### fromName(String borderTypeName) {#fromName-java.lang.String}
```
public static int fromName(String borderTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| borderTypeName | java.lang.String |  |

**Returns:**
int
### getName(int borderType) {#getName-int}
```
public static String getName(int borderType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int borderType) {#toString-int}
```
public static String toString(int borderType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
java.lang.String
