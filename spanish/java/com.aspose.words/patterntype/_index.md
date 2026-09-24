---
title: "PatternType"
linktitle: "PatternType"
second_title: "Aspose.Words para Java"
description: "Especifica el patrón de relleno que se usará para rellenar una forma en Java."
type: docs
weight: 526
url: /es/java/com.aspose.words/patterntype/
---

**Inheritance:**
java.lang.Object
```
public class PatternType
```

Especifica el patrón de relleno que se utilizará para rellenar una forma.

 **Examples:** 

Muestra cómo establecer un patrón para una forma.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [CROSS](#CROSS) | Cruz. |
| [DARK_DOWNWARD_DIAGONAL](#DARK-DOWNWARD-DIAGONAL) | Diagonal descendente oscura. |
| [DARK_HORIZONTAL](#DARK-HORIZONTAL) | Horizontal oscuro. |
| [DARK_UPWARD_DIAGONAL](#DARK-UPWARD-DIAGONAL) | Diagonal ascendente oscura. |
| [DARK_VERTICAL](#DARK-VERTICAL) | Vertical oscuro. |
| [DASHED_DOWNWARD_DIAGONAL](#DASHED-DOWNWARD-DIAGONAL) | Diagonal descendente punteada. |
| [DASHED_HORIZONTAL](#DASHED-HORIZONTAL) | Horizontal punteada. |
| [DASHED_UPWARD_DIAGONAL](#DASHED-UPWARD-DIAGONAL) | Diagonal ascendente punteada. |
| [DASHED_VERTICAL](#DASHED-VERTICAL) | Vertical punteada. |
| [DIAGONAL_BRICK](#DIAGONAL-BRICK) | Ladrillo diagonal. |
| [DIAGONAL_CROSS](#DIAGONAL-CROSS) | Cruz diagonal. |
| [DIVOT](#DIVOT) | Muesca de patrón. |
| [DOTTED_DIAMOND](#DOTTED-DIAMOND) | Diamante punteado. |
| [DOTTED_GRID](#DOTTED-GRID) | Cuadrícula punteada. |
| [DOWNWARD_DIAGONAL](#DOWNWARD-DIAGONAL) | Diagonal descendente. |
| [HORIZONTAL](#HORIZONTAL) | Horizontal. |
| [HORIZONTAL_BRICK](#HORIZONTAL-BRICK) | Ladrillo horizontal. |
| [LARGE_CHECKER_BOARD](#LARGE-CHECKER-BOARD) | Tablero de ajedrez grande. |
| [LARGE_CONFETTI](#LARGE-CONFETTI) | Confeti grande. |
| [LARGE_GRID](#LARGE-GRID) | Cuadrícula grande. |
| [LIGHT_DOWNWARD_DIAGONAL](#LIGHT-DOWNWARD-DIAGONAL) | Diagonal descendente ligera. |
| [LIGHT_HORIZONTAL](#LIGHT-HORIZONTAL) | Horizontal ligera. |
| [LIGHT_UPWARD_DIAGONAL](#LIGHT-UPWARD-DIAGONAL) | Diagonal ascendente ligera. |
| [LIGHT_VERTICAL](#LIGHT-VERTICAL) | Vertical ligera. |
| [NARROW_HORIZONTAL](#NARROW-HORIZONTAL) | Horizontal estrecha. |
| [NARROW_VERTICAL](#NARROW-VERTICAL) | Vertical estrecha. |
| [NONE](#NONE) | Sin patrón. |
| [OUTLINED_DIAMOND](#OUTLINED-DIAMOND) | Diamante contorneado. |
| [PERCENT_10](#PERCENT-10) | 10% del color de primer plano. |
| [PERCENT_20](#PERCENT-20) | 20% del color de primer plano. |
| [PERCENT_25](#PERCENT-25) | 25% del color de primer plano. |
| [PERCENT_30](#PERCENT-30) | 30% del color de primer plano. |
| [PERCENT_40](#PERCENT-40) | 40% del color de primer plano |
| [PERCENT_5](#PERCENT-5) | 5% del color de primer plano. |
| [PERCENT_50](#PERCENT-50) | 50% del color de primer plano |
| [PERCENT_60](#PERCENT-60) | 60% del color de primer plano. |
| [PERCENT_70](#PERCENT-70) | 70% del color de primer plano. |
| [PERCENT_75](#PERCENT-75) | 75% del color de primer plano. |
| [PERCENT_80](#PERCENT-80) | 80% del color de primer plano. |
| [PERCENT_90](#PERCENT-90) | 90% del color de primer plano. |
| [PLAID](#PLAID) | Cuadro escocés. |
| [SHINGLE](#SHINGLE) | Teja. |
| [SMALL_CHECKER_BOARD](#SMALL-CHECKER-BOARD) | Tablero de ajedrez pequeño. |
| [SMALL_CONFETTI](#SMALL-CONFETTI) | Confeti pequeño. |
| [SMALL_GRID](#SMALL-GRID) | Cuadrícula pequeña. |
| [SOLID_DIAMOND](#SOLID-DIAMOND) | Diamante sólido. |
| [SPHERE](#SPHERE) | Esfera. |
| [TRELLIS](#TRELLIS) | Enrejado. |
| [UPWARD_DIAGONAL](#UPWARD-DIAGONAL) | Diagonal ascendente. |
| [VERTICAL](#VERTICAL) | Vertical. |
| [WAVE](#WAVE) | Onda. |
| [WEAVE](#WEAVE) | Trama. |
| [WIDE_DOWNWARD_DIAGONAL](#WIDE-DOWNWARD-DIAGONAL) | Diagonal descendente ancha. |
| [WIDE_UPWARD_DIAGONAL](#WIDE-UPWARD-DIAGONAL) | Diagonal ascendente ancha. |
| [ZIG_ZAG](#ZIG-ZAG) | Zigzag. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String patternTypeName)](#fromName-java.lang.String) |  |
| [getName(int patternType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int patternType)](#toString-int) |  |
### CROSS {#CROSS}
```
public static int CROSS
```


Cruz.

### DARK_DOWNWARD_DIAGONAL {#DARK-DOWNWARD-DIAGONAL}
```
public static int DARK_DOWNWARD_DIAGONAL
```


Diagonal descendente oscura.

### DARK_HORIZONTAL {#DARK-HORIZONTAL}
```
public static int DARK_HORIZONTAL
```


Horizontal oscuro.

### DARK_UPWARD_DIAGONAL {#DARK-UPWARD-DIAGONAL}
```
public static int DARK_UPWARD_DIAGONAL
```


Diagonal ascendente oscura.

### DARK_VERTICAL {#DARK-VERTICAL}
```
public static int DARK_VERTICAL
```


Vertical oscuro.

### DASHED_DOWNWARD_DIAGONAL {#DASHED-DOWNWARD-DIAGONAL}
```
public static int DASHED_DOWNWARD_DIAGONAL
```


Diagonal descendente punteada.

### DASHED_HORIZONTAL {#DASHED-HORIZONTAL}
```
public static int DASHED_HORIZONTAL
```


Horizontal punteada.

### DASHED_UPWARD_DIAGONAL {#DASHED-UPWARD-DIAGONAL}
```
public static int DASHED_UPWARD_DIAGONAL
```


Diagonal ascendente punteada.

### DASHED_VERTICAL {#DASHED-VERTICAL}
```
public static int DASHED_VERTICAL
```


Vertical punteada.

### DIAGONAL_BRICK {#DIAGONAL-BRICK}
```
public static int DIAGONAL_BRICK
```


Ladrillo diagonal.

### DIAGONAL_CROSS {#DIAGONAL-CROSS}
```
public static int DIAGONAL_CROSS
```


Cruz diagonal.

### DIVOT {#DIVOT}
```
public static int DIVOT
```


Muesca de patrón.

### DOTTED_DIAMOND {#DOTTED-DIAMOND}
```
public static int DOTTED_DIAMOND
```


Diamante punteado.

### DOTTED_GRID {#DOTTED-GRID}
```
public static int DOTTED_GRID
```


Cuadrícula punteada.

### DOWNWARD_DIAGONAL {#DOWNWARD-DIAGONAL}
```
public static int DOWNWARD_DIAGONAL
```


Diagonal descendente.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Horizontal.

### HORIZONTAL_BRICK {#HORIZONTAL-BRICK}
```
public static int HORIZONTAL_BRICK
```


Ladrillo horizontal.

### LARGE_CHECKER_BOARD {#LARGE-CHECKER-BOARD}
```
public static int LARGE_CHECKER_BOARD
```


Tablero de ajedrez grande.

### LARGE_CONFETTI {#LARGE-CONFETTI}
```
public static int LARGE_CONFETTI
```


Confeti grande.

### LARGE_GRID {#LARGE-GRID}
```
public static int LARGE_GRID
```


Cuadrícula grande.

### LIGHT_DOWNWARD_DIAGONAL {#LIGHT-DOWNWARD-DIAGONAL}
```
public static int LIGHT_DOWNWARD_DIAGONAL
```


Diagonal descendente ligera.

### LIGHT_HORIZONTAL {#LIGHT-HORIZONTAL}
```
public static int LIGHT_HORIZONTAL
```


Horizontal ligera.

### LIGHT_UPWARD_DIAGONAL {#LIGHT-UPWARD-DIAGONAL}
```
public static int LIGHT_UPWARD_DIAGONAL
```


Diagonal ascendente ligera.

### LIGHT_VERTICAL {#LIGHT-VERTICAL}
```
public static int LIGHT_VERTICAL
```


Vertical ligera.

### NARROW_HORIZONTAL {#NARROW-HORIZONTAL}
```
public static int NARROW_HORIZONTAL
```


Horizontal estrecha.

### NARROW_VERTICAL {#NARROW-VERTICAL}
```
public static int NARROW_VERTICAL
```


Vertical estrecha.

### NONE {#NONE}
```
public static int NONE
```


Sin patrón.

### OUTLINED_DIAMOND {#OUTLINED-DIAMOND}
```
public static int OUTLINED_DIAMOND
```


Diamante contorneado.

### PERCENT_10 {#PERCENT-10}
```
public static int PERCENT_10
```


10% del color de primer plano.

### PERCENT_20 {#PERCENT-20}
```
public static int PERCENT_20
```


20% del color de primer plano.

### PERCENT_25 {#PERCENT-25}
```
public static int PERCENT_25
```


25% del color de primer plano.

### PERCENT_30 {#PERCENT-30}
```
public static int PERCENT_30
```


30% del color de primer plano.

### PERCENT_40 {#PERCENT-40}
```
public static int PERCENT_40
```


40% del color de primer plano

### PERCENT_5 {#PERCENT-5}
```
public static int PERCENT_5
```


5% del color de primer plano.

### PERCENT_50 {#PERCENT-50}
```
public static int PERCENT_50
```


50% del color de primer plano

### PERCENT_60 {#PERCENT-60}
```
public static int PERCENT_60
```


60% del color de primer plano.

### PERCENT_70 {#PERCENT-70}
```
public static int PERCENT_70
```


70% del color de primer plano.

### PERCENT_75 {#PERCENT-75}
```
public static int PERCENT_75
```


75% del color de primer plano.

### PERCENT_80 {#PERCENT-80}
```
public static int PERCENT_80
```


80% del color de primer plano.

### PERCENT_90 {#PERCENT-90}
```
public static int PERCENT_90
```


90% del color de primer plano.

### PLAID {#PLAID}
```
public static int PLAID
```


Cuadro escocés.

### SHINGLE {#SHINGLE}
```
public static int SHINGLE
```


Teja.

### SMALL_CHECKER_BOARD {#SMALL-CHECKER-BOARD}
```
public static int SMALL_CHECKER_BOARD
```


Tablero de ajedrez pequeño.

### SMALL_CONFETTI {#SMALL-CONFETTI}
```
public static int SMALL_CONFETTI
```


Confeti pequeño.

### SMALL_GRID {#SMALL-GRID}
```
public static int SMALL_GRID
```


Cuadrícula pequeña.

### SOLID_DIAMOND {#SOLID-DIAMOND}
```
public static int SOLID_DIAMOND
```


Diamante sólido.

### SPHERE {#SPHERE}
```
public static int SPHERE
```


Esfera.

### TRELLIS {#TRELLIS}
```
public static int TRELLIS
```


Enrejado.

### UPWARD_DIAGONAL {#UPWARD-DIAGONAL}
```
public static int UPWARD_DIAGONAL
```


Diagonal ascendente.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Vertical.

### WAVE {#WAVE}
```
public static int WAVE
```


Onda.

### WEAVE {#WEAVE}
```
public static int WEAVE
```


Trama.

### WIDE_DOWNWARD_DIAGONAL {#WIDE-DOWNWARD-DIAGONAL}
```
public static int WIDE_DOWNWARD_DIAGONAL
```


Diagonal descendente ancha.

### WIDE_UPWARD_DIAGONAL {#WIDE-UPWARD-DIAGONAL}
```
public static int WIDE_UPWARD_DIAGONAL
```


Diagonal ascendente ancha.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| patternTypeName | java.lang.String |  |

**Returns:**
int
### getName(int patternType) {#getName-int}
```
public static String getName(int patternType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| patternType | int |  |

**Returns:**
java.lang.String
