---
title: "GradientStyle"
linktitle: "GradientStyle"
second_title: "Aspose.Words per Java"
description: "Specifica lo stile per un riempimento a gradiente in Java."
type: docs
weight: 364
url: /it/java/com.aspose.words/gradientstyle/
---

**Inheritance:**
java.lang.Object
```
public class GradientStyle
```

Specifica lo stile per un riempimento a gradiente.

 **Examples:** 

Mostra come riempire una forma con un gradiente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 // Apply One-color gradient fill to the shape with ForeColor of gradient fill.
 shape.getFill().oneColorGradient(Color.RED, GradientStyle.HORIZONTAL, GradientVariant.VARIANT_2, 0.1);

 Assert.assertEquals(Color.RED.getRGB(), shape.getFill().getForeColor().getRGB());
 Assert.assertEquals(GradientStyle.HORIZONTAL, shape.getFill().getGradientStyle());
 Assert.assertEquals(GradientVariant.VARIANT_2, shape.getFill().getGradientVariant());
 Assert.assertEquals(270, shape.getFill().getGradientAngle());

 shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 // Apply Two-color gradient fill to the shape.
 shape.getFill().twoColorGradient(GradientStyle.FROM_CORNER, GradientVariant.VARIANT_4);
 // Change BackColor of gradient fill.
 shape.getFill().setBackColor(Color.YELLOW);
 // Note that changes "GradientAngle" for "GradientStyle.FromCorner/GradientStyle.FromCenter"
 // gradient fill don't get any effect, it will work only for linear gradient.
 shape.getFill().setGradientAngle(15.0);

 Assert.assertEquals(Color.YELLOW.getRGB(), shape.getFill().getBackColor().getRGB());
 Assert.assertEquals(GradientStyle.FROM_CORNER, shape.getFill().getGradientStyle());
 Assert.assertEquals(GradientVariant.VARIANT_4, shape.getFill().getGradientVariant());
 Assert.assertEquals(0, shape.getFill().getGradientAngle());

 // Use the compliance option to define the shape using DML if you want to get "GradientStyle",
 // "GradientVariant" and "GradientAngle" properties after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.GradientFill.docx", saveOptions);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [DIAGONAL_DOWN](#DIAGONAL-DOWN) | Gradiente diagonale che si sposta da un angolo superiore verso l'angolo opposto. |
| [DIAGONAL_UP](#DIAGONAL-UP) | Gradiente diagonale che si sposta da un angolo inferiore verso l'angolo opposto. |
| [FROM_CENTER](#FROM-CENTER) | Gradiente che parte dal centro verso gli angoli. |
| [FROM_CORNER](#FROM-CORNER) | Gradiente che parte da un angolo verso gli altri tre angoli. |
| [HORIZONTAL](#HORIZONTAL) | Gradiente che scorre orizzontalmente attraverso un oggetto. |
| [NONE](#NONE) | Nessun gradiente. |
| [VERTICAL](#VERTICAL) | Gradiente che scorre verticalmente su un oggetto. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String gradientStyleName)](#fromName-java.lang.String) |  |
| [getName(int gradientStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int gradientStyle)](#toString-int) |  |
### DIAGONAL_DOWN {#DIAGONAL-DOWN}
```
public static int DIAGONAL_DOWN
```


Gradiente diagonale che si sposta da un angolo superiore verso l'angolo opposto.

### DIAGONAL_UP {#DIAGONAL-UP}
```
public static int DIAGONAL_UP
```


Gradiente diagonale che si sposta da un angolo inferiore verso l'angolo opposto.

### FROM_CENTER {#FROM-CENTER}
```
public static int FROM_CENTER
```


Gradiente che parte dal centro verso gli angoli.

### FROM_CORNER {#FROM-CORNER}
```
public static int FROM_CORNER
```


Gradiente che parte da un angolo verso gli altri tre angoli.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Gradiente che scorre orizzontalmente attraverso un oggetto.

### NONE {#NONE}
```
public static int NONE
```


Nessun gradiente.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Gradiente che scorre verticalmente su un oggetto.

### length {#length}
```
public static int length
```


### fromName(String gradientStyleName) {#fromName-java.lang.String}
```
public static int fromName(String gradientStyleName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| gradientStyleName | java.lang.String |  |

**Returns:**
int
### getName(int gradientStyle) {#getName-int}
```
public static String getName(int gradientStyle)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| gradientStyle | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int gradientStyle) {#toString-int}
```
public static String toString(int gradientStyle)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| gradientStyle | int |  |

**Returns:**
java.lang.String
