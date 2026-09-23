---
title: "GradientStyle"
linktitle: "GradientStyle"
second_title: "Aspose.Words pour Java"
description: "Spécifie le style d'un remplissage en dégradé en Java."
type: docs
weight: 364
url: /fr/java/com.aspose.words/gradientstyle/
---

**Inheritance:**
java.lang.Object
```
public class GradientStyle
```

Spécifie le style d'un remplissage en dégradé.

 **Examples:** 

Montre comment remplir une forme avec des dégradés.

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
## Champs

| Champ | Description |
| --- | --- |
| [DIAGONAL_DOWN](#DIAGONAL-DOWN) | Dégradé diagonal allant du coin supérieur vers le coin opposé. |
| [DIAGONAL_UP](#DIAGONAL-UP) | Dégradé diagonal allant du coin inférieur vers le coin opposé. |
| [FROM_CENTER](#FROM-CENTER) | Dégradé s'étendant du centre vers les coins. |
| [FROM_CORNER](#FROM-CORNER) | Dégradé partant d'un coin vers les trois autres coins. |
| [HORIZONTAL](#HORIZONTAL) | Dégradé s'étendant horizontalement à travers un objet. |
| [NONE](#NONE) | Pas de dégradé. |
| [VERTICAL](#VERTICAL) | Dégradé s'étendant verticalement le long d'un objet. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String gradientStyleName)](#fromName-java.lang.String) |  |
| [getName(int gradientStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int gradientStyle)](#toString-int) |  |
### DIAGONAL_DOWN {#DIAGONAL-DOWN}
```
public static int DIAGONAL_DOWN
```


Dégradé diagonal allant du coin supérieur vers le coin opposé.

### DIAGONAL_UP {#DIAGONAL-UP}
```
public static int DIAGONAL_UP
```


Dégradé diagonal allant du coin inférieur vers le coin opposé.

### FROM_CENTER {#FROM-CENTER}
```
public static int FROM_CENTER
```


Dégradé s'étendant du centre vers les coins.

### FROM_CORNER {#FROM-CORNER}
```
public static int FROM_CORNER
```


Dégradé partant d'un coin vers les trois autres coins.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Dégradé s'étendant horizontalement à travers un objet.

### NONE {#NONE}
```
public static int NONE
```


Pas de dégradé.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Dégradé s'étendant verticalement le long d'un objet.

### length {#length}
```
public static int length
```


### fromName(String gradientStyleName) {#fromName-java.lang.String}
```
public static int fromName(String gradientStyleName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| gradientStyleName | java.lang.String |  |

**Returns:**
int
### getName(int gradientStyle) {#getName-int}
```
public static String getName(int gradientStyle)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| gradientStyle | int |  |

**Returns:**
java.lang.String
