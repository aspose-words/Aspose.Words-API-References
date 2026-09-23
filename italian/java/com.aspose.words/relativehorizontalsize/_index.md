---
title: "RelativeHorizontalSize"
linktitle: "RelativeHorizontalSize"
second_title: "Aspose.Words per Java"
description: "Specifica rispetto a cosa la larghezza di una forma o di un riquadro di testo viene calcolata orizzontalmente in Java."
type: docs
weight: 562
url: /it/java/com.aspose.words/relativehorizontalsize/
---

**Inheritance:**
java.lang.Object
```
public class RelativeHorizontalSize
```

Specifica rispetto a cosa la larghezza di una forma o di un riquadro di testo è calcolata orizzontalmente.

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
| [DEFAULT](#DEFAULT) | Il valore predefinito è [MARGIN](../../com.aspose.words/relativehorizontalsize/\#MARGIN). |
| [INNER_MARGIN](#INNER-MARGIN) | Specifica che la larghezza è calcolata relativamente alla dimensione dell'area del margine interno, alla dimensione dell'area del margine sinistro per le pagine dispari e alla dimensione dell'area del margine destro per le pagine pari. |
| [LEFT_MARGIN](#LEFT-MARGIN) | Specifica che la larghezza è calcolata relativamente alla dimensione dell'area del margine sinistro. |
| [MARGIN](#MARGIN) | Specifica che la larghezza è calcolata relativamente allo spazio tra i margini sinistro e destro. |
| [OUTER_MARGIN](#OUTER-MARGIN) | Specifica che la larghezza è calcolata relativamente alle dimensioni dell'area del margine esterno, alle dimensioni dell'area del margine destro per le pagine dispari e alle dimensioni dell'area del margine sinistro per le pagine pari. |
| [PAGE](#PAGE) | Specifica che la larghezza è calcolata relativamente alla larghezza della pagina. |
| [RIGHT_MARGIN](#RIGHT-MARGIN) | Specifica che la larghezza è calcolata relativamente alle dimensioni dell'area del margine destro. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String relativeHorizontalSizeName)](#fromName-java.lang.String) |  |
| [getName(int relativeHorizontalSize)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeHorizontalSize)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Il valore predefinito è [MARGIN](../../com.aspose.words/relativehorizontalsize/\#MARGIN).

### INNER_MARGIN {#INNER-MARGIN}
```
public static int INNER_MARGIN
```


Specifica che la larghezza è calcolata relativamente alla dimensione dell'area del margine interno, alla dimensione dell'area del margine sinistro per le pagine dispari e alla dimensione dell'area del margine destro per le pagine pari.

### LEFT_MARGIN {#LEFT-MARGIN}
```
public static int LEFT_MARGIN
```


Specifica che la larghezza è calcolata relativamente alla dimensione dell'area del margine sinistro.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Specifica che la larghezza è calcolata relativamente allo spazio tra i margini sinistro e destro.

### OUTER_MARGIN {#OUTER-MARGIN}
```
public static int OUTER_MARGIN
```


Specifica che la larghezza è calcolata relativamente alle dimensioni dell'area del margine esterno, alle dimensioni dell'area del margine destro per le pagine dispari e alle dimensioni dell'area del margine sinistro per le pagine pari.

### PAGE {#PAGE}
```
public static int PAGE
```


Specifica che la larghezza è calcolata relativamente alla larghezza della pagina.

### RIGHT_MARGIN {#RIGHT-MARGIN}
```
public static int RIGHT_MARGIN
```


Specifica che la larghezza è calcolata relativamente alle dimensioni dell'area del margine destro.

### length {#length}
```
public static int length
```


### fromName(String relativeHorizontalSizeName) {#fromName-java.lang.String}
```
public static int fromName(String relativeHorizontalSizeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| relativeHorizontalSizeName | java.lang.String |  |

**Returns:**
int
### getName(int relativeHorizontalSize) {#getName-int}
```
public static String getName(int relativeHorizontalSize)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| relativeHorizontalSize | int |  |

**Returns:**
java.lang.String
