---
title: "GradientStyle"
linktitle: "GradientStyle"
second_title: "Aspose.Words für Java"
description: "Gibt den Stil für eine Farbverlauf‑Füllung in Java an."
type: docs
weight: 364
url: /de/java/com.aspose.words/gradientstyle/
---

**Inheritance:**
java.lang.Object
```
public class GradientStyle
```

Gibt den Stil für eine Farbverlaufsfüllung an.

 **Examples:** 

Zeigt, wie man eine Form mit Farbverläufen füllt.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [DIAGONAL_DOWN](#DIAGONAL-DOWN) | Diagonaler Farbverlauf, der von einer oberen Ecke zur gegenüberliegenden Ecke verläuft. |
| [DIAGONAL_UP](#DIAGONAL-UP) | Diagonaler Farbverlauf, der von einer unteren Ecke zur gegenüberliegenden Ecke aufsteigt. |
| [FROM_CENTER](#FROM-CENTER) | Farbverlauf, der vom Zentrum zu den Ecken verläuft. |
| [FROM_CORNER](#FROM-CORNER) | Farbverlauf, der von einer Ecke zu den anderen drei Ecken verläuft. |
| [HORIZONTAL](#HORIZONTAL) | Farbverlauf, der horizontal über ein Objekt verläuft. |
| [NONE](#NONE) | Kein Farbverlauf. |
| [VERTICAL](#VERTICAL) | Farbverlauf, der vertikal über ein Objekt verläuft. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String gradientStyleName)](#fromName-java.lang.String) |  |
| [getName(int gradientStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int gradientStyle)](#toString-int) |  |
### DIAGONAL_DOWN {#DIAGONAL-DOWN}
```
public static int DIAGONAL_DOWN
```


Diagonaler Farbverlauf, der von einer oberen Ecke zur gegenüberliegenden Ecke verläuft.

### DIAGONAL_UP {#DIAGONAL-UP}
```
public static int DIAGONAL_UP
```


Diagonaler Farbverlauf, der von einer unteren Ecke zur gegenüberliegenden Ecke aufsteigt.

### FROM_CENTER {#FROM-CENTER}
```
public static int FROM_CENTER
```


Farbverlauf, der vom Zentrum zu den Ecken verläuft.

### FROM_CORNER {#FROM-CORNER}
```
public static int FROM_CORNER
```


Farbverlauf, der von einer Ecke zu den anderen drei Ecken verläuft.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Farbverlauf, der horizontal über ein Objekt verläuft.

### NONE {#NONE}
```
public static int NONE
```


Kein Farbverlauf.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Farbverlauf, der vertikal über ein Objekt verläuft.

### length {#length}
```
public static int length
```


### fromName(String gradientStyleName) {#fromName-java.lang.String}
```
public static int fromName(String gradientStyleName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| gradientStyleName | java.lang.String |  |

**Returns:**
int
### getName(int gradientStyle) {#getName-int}
```
public static String getName(int gradientStyle)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| gradientStyle | int |  |

**Returns:**
java.lang.String
