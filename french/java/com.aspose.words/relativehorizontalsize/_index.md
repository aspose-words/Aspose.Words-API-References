---
title: "RelativeHorizontalSize"
linktitle: "RelativeHorizontalSize"
second_title: "Aspose.Words pour Java"
description: "Spécifie par rapport à quoi la largeur d'une forme ou d'un cadre de texte est calculée horizontalement en Java."
type: docs
weight: 562
url: /fr/java/com.aspose.words/relativehorizontalsize/
---

**Inheritance:**
java.lang.Object
```
public class RelativeHorizontalSize
```

Spécifie relativement à quoi la largeur d'une forme ou d'un cadre de texte est calculée horizontalement.

 **Examples:** 

Montre comment définir la taille et la position relatives.

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
## Champs

| Champ | Description |
| --- | --- |
| [DEFAULT](#DEFAULT) | La valeur par défaut est [MARGIN](../../com.aspose.words/relativehorizontalsize/\#MARGIN). |
| [INNER_MARGIN](#INNER-MARGIN) | Spécifie que la largeur est calculée relativement à la taille de la zone de marge intérieure, à la taille de la marge gauche pour les pages impaires et à la taille de la marge droite pour les pages paires. |
| [LEFT_MARGIN](#LEFT-MARGIN) | Spécifie que la largeur est calculée relativement à la taille de la marge gauche. |
| [MARGIN](#MARGIN) | Spécifie que la largeur est calculée relativement à l'espace entre les marges gauche et droite. |
| [OUTER_MARGIN](#OUTER-MARGIN) | Spécifie que la largeur est calculée relativement à la taille de la zone de marge extérieure, à la taille de la zone de marge droite pour les pages impaires et à la taille de la zone de marge gauche pour les pages paires. |
| [PAGE](#PAGE) | Spécifie que la largeur est calculée relativement à la largeur de la page. |
| [RIGHT_MARGIN](#RIGHT-MARGIN) | Spécifie que la largeur est calculée relativement à la taille de la zone de marge droite. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String relativeHorizontalSizeName)](#fromName-java.lang.String) |  |
| [getName(int relativeHorizontalSize)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeHorizontalSize)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


La valeur par défaut est [MARGIN](../../com.aspose.words/relativehorizontalsize/\#MARGIN).

### INNER_MARGIN {#INNER-MARGIN}
```
public static int INNER_MARGIN
```


Spécifie que la largeur est calculée relativement à la taille de la zone de marge intérieure, à la taille de la marge gauche pour les pages impaires et à la taille de la marge droite pour les pages paires.

### LEFT_MARGIN {#LEFT-MARGIN}
```
public static int LEFT_MARGIN
```


Spécifie que la largeur est calculée relativement à la taille de la marge gauche.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Spécifie que la largeur est calculée relativement à l'espace entre les marges gauche et droite.

### OUTER_MARGIN {#OUTER-MARGIN}
```
public static int OUTER_MARGIN
```


Spécifie que la largeur est calculée relativement à la taille de la zone de marge extérieure, à la taille de la zone de marge droite pour les pages impaires et à la taille de la zone de marge gauche pour les pages paires.

### PAGE {#PAGE}
```
public static int PAGE
```


Spécifie que la largeur est calculée relativement à la largeur de la page.

### RIGHT_MARGIN {#RIGHT-MARGIN}
```
public static int RIGHT_MARGIN
```


Spécifie que la largeur est calculée relativement à la taille de la zone de marge droite.

### length {#length}
```
public static int length
```


### fromName(String relativeHorizontalSizeName) {#fromName-java.lang.String}
```
public static int fromName(String relativeHorizontalSizeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| relativeHorizontalSizeName | java.lang.String |  |

**Returns:**
int
### getName(int relativeHorizontalSize) {#getName-int}
```
public static String getName(int relativeHorizontalSize)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| relativeHorizontalSize | int |  |

**Returns:**
java.lang.String
