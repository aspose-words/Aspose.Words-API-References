---
title: "RelativeVerticalSize"
linktitle: "RelativeVerticalSize"
second_title: "Aspose.Words per Java"
description: "Specifica rispetto a cosa l'altezza di una forma o di un riquadro di testo viene calcolata verticalmente in Java."
type: docs
weight: 564
url: /it/java/com.aspose.words/relativeverticalsize/
---

**Inheritance:**
java.lang.Object
```
public class RelativeVerticalSize
```

Specifica rispetto a cosa l'altezza di una forma o di un riquadro di testo è calcolata verticalmente.

 **Examples:** 

Mostra come impostare dimensione e posizione relative.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [BOTTOM_MARGIN](#BOTTOM-MARGIN) | Specifica che l'altezza viene calcolata relativamente alle dimensioni dell'area del margine inferiore. |
| [DEFAULT](#DEFAULT) | Il valore predefinito è [MARGIN](../../com.aspose.words/relativeverticalsize/\#MARGIN). |
| [INNER_MARGIN](#INNER-MARGIN) | Specifica che l'altezza viene calcolata relativamente alle dimensioni dell'area del margine interno, alle dimensioni dell'area del margine superiore per le pagine dispari e alle dimensioni dell'area del margine inferiore per le pagine pari. |
| [MARGIN](#MARGIN) | Specifica che l'altezza viene calcolata relativamente allo spazio tra i margini superiore e inferiore. |
| [OUTER_MARGIN](#OUTER-MARGIN) | Specifica che l'altezza viene calcolata relativamente alle dimensioni dell'area del margine esterno, alle dimensioni dell'area del margine inferiore per le pagine dispari e alle dimensioni dell'area del margine superiore per le pagine pari. |
| [PAGE](#PAGE) | Specifica che l'altezza viene calcolata relativamente all'altezza della pagina. |
| [TOP_MARGIN](#TOP-MARGIN) | Specifica che l'altezza viene calcolata relativamente alle dimensioni dell'area del margine superiore. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String relativeVerticalSizeName)](#fromName-java.lang.String) |  |
| [getName(int relativeVerticalSize)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeVerticalSize)](#toString-int) |  |
### BOTTOM_MARGIN {#BOTTOM-MARGIN}
```
public static int BOTTOM_MARGIN
```


Specifica che l'altezza viene calcolata relativamente alle dimensioni dell'area del margine inferiore.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Il valore predefinito è [MARGIN](../../com.aspose.words/relativeverticalsize/\#MARGIN).

### INNER_MARGIN {#INNER-MARGIN}
```
public static int INNER_MARGIN
```


Specifica che l'altezza viene calcolata relativamente alle dimensioni dell'area del margine interno, alle dimensioni dell'area del margine superiore per le pagine dispari e alle dimensioni dell'area del margine inferiore per le pagine pari.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Specifica che l'altezza viene calcolata relativamente allo spazio tra i margini superiore e inferiore.

### OUTER_MARGIN {#OUTER-MARGIN}
```
public static int OUTER_MARGIN
```


Specifica che l'altezza viene calcolata relativamente alle dimensioni dell'area del margine esterno, alle dimensioni dell'area del margine inferiore per le pagine dispari e alle dimensioni dell'area del margine superiore per le pagine pari.

### PAGE {#PAGE}
```
public static int PAGE
```


Specifica che l'altezza viene calcolata relativamente all'altezza della pagina.

### TOP_MARGIN {#TOP-MARGIN}
```
public static int TOP_MARGIN
```


Specifica che l'altezza viene calcolata relativamente alle dimensioni dell'area del margine superiore.

### length {#length}
```
public static int length
```


### fromName(String relativeVerticalSizeName) {#fromName-java.lang.String}
```
public static int fromName(String relativeVerticalSizeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| relativeVerticalSizeName | java.lang.String |  |

**Returns:**
int
### getName(int relativeVerticalSize) {#getName-int}
```
public static String getName(int relativeVerticalSize)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| relativeVerticalSize | int |  |

**Returns:**
java.lang.String
