---
title: "BorderType"
linktitle: "BorderType"
second_title: "Aspose.Words pour Java"
description: "Spécifie les côtés d'une bordure en Java."
type: docs
weight: 48
url: /fr/java/com.aspose.words/bordertype/
---

**Inheritance:**
java.lang.Object
```
public class BorderType
```

Spécifie les côtés d'une bordure.

Pour en savoir plus, consultez l'article de documentation [ Programming with Documents ][Programming with Documents].

 **Examples:** 

Montre comment insérer un paragraphe avec une bordure supérieure.

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
## Champs

| Champ | Description |
| --- | --- |
| [BOTTOM](#BOTTOM) | Spécifie la bordure inférieure d'un paragraphe ou d'une cellule de tableau. |
| [DIAGONAL_DOWN](#DIAGONAL-DOWN) | Spécifie la bordure diagonale d'une cellule de tableau. |
| [DIAGONAL_UP](#DIAGONAL-UP) | Spécifie la bordure diagonale d'une cellule de tableau. |
| [HORIZONTAL](#HORIZONTAL) | Spécifie la bordure horizontale entre les cellules d'un tableau ou entre les paragraphes correspondants. |
| [LEFT](#LEFT) | Spécifie la bordure gauche d'un paragraphe ou d'une cellule de tableau. |
| [NONE](#NONE) | Valeur par défaut. |
| [RIGHT](#RIGHT) | Spécifie la bordure droite d'un paragraphe ou d'une cellule de tableau. |
| [TOP](#TOP) | Spécifie la bordure supérieure d'un paragraphe ou d'une cellule de tableau. |
| [VERTICAL](#VERTICAL) | Spécifie la bordure verticale entre les cellules d'un tableau. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String borderTypeName)](#fromName-java.lang.String) |  |
| [getName(int borderType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int borderType)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Spécifie la bordure inférieure d'un paragraphe ou d'une cellule de tableau.

### DIAGONAL_DOWN {#DIAGONAL-DOWN}
```
public static int DIAGONAL_DOWN
```


Spécifie la bordure diagonale d'une cellule de tableau.

### DIAGONAL_UP {#DIAGONAL-UP}
```
public static int DIAGONAL_UP
```


Spécifie la bordure diagonale d'une cellule de tableau.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Spécifie la bordure horizontale entre les cellules d'un tableau ou entre les paragraphes correspondants.

### LEFT {#LEFT}
```
public static int LEFT
```


Spécifie la bordure gauche d'un paragraphe ou d'une cellule de tableau.

### NONE {#NONE}
```
public static int NONE
```


Valeur par défaut.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Spécifie la bordure droite d'un paragraphe ou d'une cellule de tableau.

### TOP {#TOP}
```
public static int TOP
```


Spécifie la bordure supérieure d'un paragraphe ou d'une cellule de tableau.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Spécifie la bordure verticale entre les cellules d'un tableau.

### length {#length}
```
public static int length
```


### fromName(String borderTypeName) {#fromName-java.lang.String}
```
public static int fromName(String borderTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| borderTypeName | java.lang.String |  |

**Returns:**
int
### getName(int borderType) {#getName-int}
```
public static String getName(int borderType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
java.lang.String
