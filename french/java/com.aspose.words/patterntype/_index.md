---
title: "PatternType"
linktitle: "PatternType"
second_title: "Aspose.Words pour Java"
description: "Spécifie le motif de remplissage à utiliser pour remplir une forme en Java."
type: docs
weight: 526
url: /fr/java/com.aspose.words/patterntype/
---

**Inheritance:**
java.lang.Object
```
public class PatternType
```

Spécifie le motif de remplissage à utiliser pour remplir une forme.

 **Examples:** 

Montre comment définir un motif pour une forme.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Fill fill = shape.getFill();

 System.out.println(MessageFormat.format("Pattern value is: {0}",fill.getPattern()));

 // There are several ways specified fill to a pattern.
 // 1 -  Apply pattern to the shape fill:
 fill.patterned(PatternType.DIAGONAL_BRICK);

 // 2 -  Apply pattern with foreground and background colors to the shape fill:
 fill.patterned(PatternType.DIAGONAL_BRICK, Color.yellow, Color.blue);

 doc.save(getArtifactsDir() + "Shape.FillPattern.docx");
 
```
## Champs

| Champ | Description |
| --- | --- |
| [CROSS](#CROSS) | Croix. |
| [DARK_DOWNWARD_DIAGONAL](#DARK-DOWNWARD-DIAGONAL) | Diagonale descendante sombre. |
| [DARK_HORIZONTAL](#DARK-HORIZONTAL) | Horizontal sombre. |
| [DARK_UPWARD_DIAGONAL](#DARK-UPWARD-DIAGONAL) | Diagonale ascendante sombre. |
| [DARK_VERTICAL](#DARK-VERTICAL) | Vertical sombre. |
| [DASHED_DOWNWARD_DIAGONAL](#DASHED-DOWNWARD-DIAGONAL) | Diagonale descendante en pointillés. |
| [DASHED_HORIZONTAL](#DASHED-HORIZONTAL) | Horizontal en pointillés. |
| [DASHED_UPWARD_DIAGONAL](#DASHED-UPWARD-DIAGONAL) | Diagonale ascendante en pointillés. |
| [DASHED_VERTICAL](#DASHED-VERTICAL) | Vertical en pointillés. |
| [DIAGONAL_BRICK](#DIAGONAL-BRICK) | Brique diagonale. |
| [DIAGONAL_CROSS](#DIAGONAL-CROSS) | Croix diagonale. |
| [DIVOT](#DIVOT) | Motif en creux. |
| [DOTTED_DIAMOND](#DOTTED-DIAMOND) | Losange pointillé. |
| [DOTTED_GRID](#DOTTED-GRID) | Grille pointillée. |
| [DOWNWARD_DIAGONAL](#DOWNWARD-DIAGONAL) | Diagonale descendante. |
| [HORIZONTAL](#HORIZONTAL) | Horizontal. |
| [HORIZONTAL_BRICK](#HORIZONTAL-BRICK) | Brique horizontale. |
| [LARGE_CHECKER_BOARD](#LARGE-CHECKER-BOARD) | Grand damier. |
| [LARGE_CONFETTI](#LARGE-CONFETTI) | Grand confettis. |
| [LARGE_GRID](#LARGE-GRID) | Grande grille. |
| [LIGHT_DOWNWARD_DIAGONAL](#LIGHT-DOWNWARD-DIAGONAL) | Diagonale descendante légère. |
| [LIGHT_HORIZONTAL](#LIGHT-HORIZONTAL) | Horizontal léger. |
| [LIGHT_UPWARD_DIAGONAL](#LIGHT-UPWARD-DIAGONAL) | Diagonale ascendante légère. |
| [LIGHT_VERTICAL](#LIGHT-VERTICAL) | Vertical léger. |
| [NARROW_HORIZONTAL](#NARROW-HORIZONTAL) | Horizontal étroit. |
| [NARROW_VERTICAL](#NARROW-VERTICAL) | Vertical étroit. |
| [NONE](#NONE) | Aucun motif. |
| [OUTLINED_DIAMOND](#OUTLINED-DIAMOND) | Losange contourné. |
| [PERCENT_10](#PERCENT-10) | 10% de la couleur de premier plan. |
| [PERCENT_20](#PERCENT-20) | 20% de la couleur de premier plan. |
| [PERCENT_25](#PERCENT-25) | 25% de la couleur de premier plan. |
| [PERCENT_30](#PERCENT-30) | 30% de la couleur de premier plan. |
| [PERCENT_40](#PERCENT-40) | 40% de la couleur de premier plan |
| [PERCENT_5](#PERCENT-5) | 5% de la couleur de premier plan. |
| [PERCENT_50](#PERCENT-50) | 50% de la couleur de premier plan |
| [PERCENT_60](#PERCENT-60) | 60% de la couleur de premier plan. |
| [PERCENT_70](#PERCENT-70) | 70% de la couleur de premier plan. |
| [PERCENT_75](#PERCENT-75) | 75% de la couleur de premier plan. |
| [PERCENT_80](#PERCENT-80) | 80% de la couleur de premier plan. |
| [PERCENT_90](#PERCENT-90) | 90% de la couleur de premier plan. |
| [PLAID](#PLAID) | Carreau. |
| [SHINGLE](#SHINGLE) | Bardeau. |
| [SMALL_CHECKER_BOARD](#SMALL-CHECKER-BOARD) | Petit damier. |
| [SMALL_CONFETTI](#SMALL-CONFETTI) | Petits confettis. |
| [SMALL_GRID](#SMALL-GRID) | Petite grille. |
| [SOLID_DIAMOND](#SOLID-DIAMOND) | Losange plein. |
| [SPHERE](#SPHERE) | Sphère. |
| [TRELLIS](#TRELLIS) | Treillis. |
| [UPWARD_DIAGONAL](#UPWARD-DIAGONAL) | Diagonale ascendante. |
| [VERTICAL](#VERTICAL) | Vertical. |
| [WAVE](#WAVE) | Vague. |
| [WEAVE](#WEAVE) | Tissage. |
| [WIDE_DOWNWARD_DIAGONAL](#WIDE-DOWNWARD-DIAGONAL) | Diagonale descendante large. |
| [WIDE_UPWARD_DIAGONAL](#WIDE-UPWARD-DIAGONAL) | Diagonale ascendante large. |
| [ZIG_ZAG](#ZIG-ZAG) | Zigzag. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String patternTypeName)](#fromName-java.lang.String) |  |
| [getName(int patternType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int patternType)](#toString-int) |  |
### CROSS {#CROSS}
```
public static int CROSS
```


Croix.

### DARK_DOWNWARD_DIAGONAL {#DARK-DOWNWARD-DIAGONAL}
```
public static int DARK_DOWNWARD_DIAGONAL
```


Diagonale descendante sombre.

### DARK_HORIZONTAL {#DARK-HORIZONTAL}
```
public static int DARK_HORIZONTAL
```


Horizontal sombre.

### DARK_UPWARD_DIAGONAL {#DARK-UPWARD-DIAGONAL}
```
public static int DARK_UPWARD_DIAGONAL
```


Diagonale ascendante sombre.

### DARK_VERTICAL {#DARK-VERTICAL}
```
public static int DARK_VERTICAL
```


Vertical sombre.

### DASHED_DOWNWARD_DIAGONAL {#DASHED-DOWNWARD-DIAGONAL}
```
public static int DASHED_DOWNWARD_DIAGONAL
```


Diagonale descendante en pointillés.

### DASHED_HORIZONTAL {#DASHED-HORIZONTAL}
```
public static int DASHED_HORIZONTAL
```


Horizontal en pointillés.

### DASHED_UPWARD_DIAGONAL {#DASHED-UPWARD-DIAGONAL}
```
public static int DASHED_UPWARD_DIAGONAL
```


Diagonale ascendante en pointillés.

### DASHED_VERTICAL {#DASHED-VERTICAL}
```
public static int DASHED_VERTICAL
```


Vertical en pointillés.

### DIAGONAL_BRICK {#DIAGONAL-BRICK}
```
public static int DIAGONAL_BRICK
```


Brique diagonale.

### DIAGONAL_CROSS {#DIAGONAL-CROSS}
```
public static int DIAGONAL_CROSS
```


Croix diagonale.

### DIVOT {#DIVOT}
```
public static int DIVOT
```


Motif en creux.

### DOTTED_DIAMOND {#DOTTED-DIAMOND}
```
public static int DOTTED_DIAMOND
```


Losange pointillé.

### DOTTED_GRID {#DOTTED-GRID}
```
public static int DOTTED_GRID
```


Grille pointillée.

### DOWNWARD_DIAGONAL {#DOWNWARD-DIAGONAL}
```
public static int DOWNWARD_DIAGONAL
```


Diagonale descendante.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Horizontal.

### HORIZONTAL_BRICK {#HORIZONTAL-BRICK}
```
public static int HORIZONTAL_BRICK
```


Brique horizontale.

### LARGE_CHECKER_BOARD {#LARGE-CHECKER-BOARD}
```
public static int LARGE_CHECKER_BOARD
```


Grand damier.

### LARGE_CONFETTI {#LARGE-CONFETTI}
```
public static int LARGE_CONFETTI
```


Grand confettis.

### LARGE_GRID {#LARGE-GRID}
```
public static int LARGE_GRID
```


Grande grille.

### LIGHT_DOWNWARD_DIAGONAL {#LIGHT-DOWNWARD-DIAGONAL}
```
public static int LIGHT_DOWNWARD_DIAGONAL
```


Diagonale descendante légère.

### LIGHT_HORIZONTAL {#LIGHT-HORIZONTAL}
```
public static int LIGHT_HORIZONTAL
```


Horizontal léger.

### LIGHT_UPWARD_DIAGONAL {#LIGHT-UPWARD-DIAGONAL}
```
public static int LIGHT_UPWARD_DIAGONAL
```


Diagonale ascendante légère.

### LIGHT_VERTICAL {#LIGHT-VERTICAL}
```
public static int LIGHT_VERTICAL
```


Vertical léger.

### NARROW_HORIZONTAL {#NARROW-HORIZONTAL}
```
public static int NARROW_HORIZONTAL
```


Horizontal étroit.

### NARROW_VERTICAL {#NARROW-VERTICAL}
```
public static int NARROW_VERTICAL
```


Vertical étroit.

### NONE {#NONE}
```
public static int NONE
```


Aucun motif.

### OUTLINED_DIAMOND {#OUTLINED-DIAMOND}
```
public static int OUTLINED_DIAMOND
```


Losange contourné.

### PERCENT_10 {#PERCENT-10}
```
public static int PERCENT_10
```


10% de la couleur de premier plan.

### PERCENT_20 {#PERCENT-20}
```
public static int PERCENT_20
```


20% de la couleur de premier plan.

### PERCENT_25 {#PERCENT-25}
```
public static int PERCENT_25
```


25% de la couleur de premier plan.

### PERCENT_30 {#PERCENT-30}
```
public static int PERCENT_30
```


30% de la couleur de premier plan.

### PERCENT_40 {#PERCENT-40}
```
public static int PERCENT_40
```


40% de la couleur de premier plan

### PERCENT_5 {#PERCENT-5}
```
public static int PERCENT_5
```


5% de la couleur de premier plan.

### PERCENT_50 {#PERCENT-50}
```
public static int PERCENT_50
```


50% de la couleur de premier plan

### PERCENT_60 {#PERCENT-60}
```
public static int PERCENT_60
```


60% de la couleur de premier plan.

### PERCENT_70 {#PERCENT-70}
```
public static int PERCENT_70
```


70% de la couleur de premier plan.

### PERCENT_75 {#PERCENT-75}
```
public static int PERCENT_75
```


75% de la couleur de premier plan.

### PERCENT_80 {#PERCENT-80}
```
public static int PERCENT_80
```


80% de la couleur de premier plan.

### PERCENT_90 {#PERCENT-90}
```
public static int PERCENT_90
```


90% de la couleur de premier plan.

### PLAID {#PLAID}
```
public static int PLAID
```


Carreau.

### SHINGLE {#SHINGLE}
```
public static int SHINGLE
```


Bardeau.

### SMALL_CHECKER_BOARD {#SMALL-CHECKER-BOARD}
```
public static int SMALL_CHECKER_BOARD
```


Petit damier.

### SMALL_CONFETTI {#SMALL-CONFETTI}
```
public static int SMALL_CONFETTI
```


Petits confettis.

### SMALL_GRID {#SMALL-GRID}
```
public static int SMALL_GRID
```


Petite grille.

### SOLID_DIAMOND {#SOLID-DIAMOND}
```
public static int SOLID_DIAMOND
```


Losange plein.

### SPHERE {#SPHERE}
```
public static int SPHERE
```


Sphère.

### TRELLIS {#TRELLIS}
```
public static int TRELLIS
```


Treillis.

### UPWARD_DIAGONAL {#UPWARD-DIAGONAL}
```
public static int UPWARD_DIAGONAL
```


Diagonale ascendante.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Vertical.

### WAVE {#WAVE}
```
public static int WAVE
```


Vague.

### WEAVE {#WEAVE}
```
public static int WEAVE
```


Tissage.

### WIDE_DOWNWARD_DIAGONAL {#WIDE-DOWNWARD-DIAGONAL}
```
public static int WIDE_DOWNWARD_DIAGONAL
```


Diagonale descendante large.

### WIDE_UPWARD_DIAGONAL {#WIDE-UPWARD-DIAGONAL}
```
public static int WIDE_UPWARD_DIAGONAL
```


Diagonale ascendante large.

### ZIG_ZAG {#ZIG-ZAG}
```
public static int ZIG_ZAG
```


Zigzag.

### length {#length}
```
public static int length
```


### fromName(String patternTypeName) {#fromName-java.lang.String}
```
public static int fromName(String patternTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| patternTypeName | java.lang.String |  |

**Returns:**
int
### getName(int patternType) {#getName-int}
```
public static String getName(int patternType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| patternType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int patternType) {#toString-int}
```
public static String toString(int patternType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| patternType | int |  |

**Returns:**
java.lang.String
