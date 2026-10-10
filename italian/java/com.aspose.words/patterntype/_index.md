---
title: "PatternType"
linktitle: "PatternType"
second_title: "Aspose.Words per Java"
description: "Specifica il modello di riempimento da utilizzare per riempire una forma in Java."
type: docs
weight: 526
url: /it/java/com.aspose.words/patterntype/
---

**Inheritance:**
java.lang.Object
```
public class PatternType
```

Specifica il modello di riempimento da utilizzare per riempire una forma.

 **Examples:** 

Mostra come impostare il motivo per una forma.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [CROSS](#CROSS) | Croce. |
| [DARK_DOWNWARD_DIAGONAL](#DARK-DOWNWARD-DIAGONAL) | Diagonale discendente scura. |
| [DARK_HORIZONTAL](#DARK-HORIZONTAL) | Orizzontale scura. |
| [DARK_UPWARD_DIAGONAL](#DARK-UPWARD-DIAGONAL) | Diagonale ascendente scura. |
| [DARK_VERTICAL](#DARK-VERTICAL) | Verticale scura. |
| [DASHED_DOWNWARD_DIAGONAL](#DASHED-DOWNWARD-DIAGONAL) | Diagonale discendente tratteggiata. |
| [DASHED_HORIZONTAL](#DASHED-HORIZONTAL) | Orizzontale tratteggiata. |
| [DASHED_UPWARD_DIAGONAL](#DASHED-UPWARD-DIAGONAL) | Diagonale ascendente tratteggiata. |
| [DASHED_VERTICAL](#DASHED-VERTICAL) | Verticale tratteggiata. |
| [DIAGONAL_BRICK](#DIAGONAL-BRICK) | Mattone diagonale. |
| [DIAGONAL_CROSS](#DIAGONAL-CROSS) | Croce diagonale. |
| [DIVOT](#DIVOT) | Incavatura del modello. |
| [DOTTED_DIAMOND](#DOTTED-DIAMOND) | Diamante punteggiato. |
| [DOTTED_GRID](#DOTTED-GRID) | Griglia punteggiata. |
| [DOWNWARD_DIAGONAL](#DOWNWARD-DIAGONAL) | Diagonale discendente. |
| [HORIZONTAL](#HORIZONTAL) | Orizzontale. |
| [HORIZONTAL_BRICK](#HORIZONTAL-BRICK) | Mattone orizzontale. |
| [LARGE_CHECKER_BOARD](#LARGE-CHECKER-BOARD) | Grande scacchiera. |
| [LARGE_CONFETTI](#LARGE-CONFETTI) | Grande confetti. |
| [LARGE_GRID](#LARGE-GRID) | Griglia grande. |
| [LIGHT_DOWNWARD_DIAGONAL](#LIGHT-DOWNWARD-DIAGONAL) | Diagonale leggera verso il basso. |
| [LIGHT_HORIZONTAL](#LIGHT-HORIZONTAL) | Orizzontale leggera. |
| [LIGHT_UPWARD_DIAGONAL](#LIGHT-UPWARD-DIAGONAL) | Diagonale leggera verso l'alto. |
| [LIGHT_VERTICAL](#LIGHT-VERTICAL) | Verticale leggera. |
| [NARROW_HORIZONTAL](#NARROW-HORIZONTAL) | Orizzontale stretta. |
| [NARROW_VERTICAL](#NARROW-VERTICAL) | Verticale stretta. |
| [NONE](#NONE) | Nessun motivo. |
| [OUTLINED_DIAMOND](#OUTLINED-DIAMOND) | Diamante contornato. |
| [PERCENT_10](#PERCENT-10) | 10% del colore di primo piano. |
| [PERCENT_20](#PERCENT-20) | 20% del colore di primo piano. |
| [PERCENT_25](#PERCENT-25) | 25% del colore di primo piano. |
| [PERCENT_30](#PERCENT-30) | 30% del colore di primo piano. |
| [PERCENT_40](#PERCENT-40) | 40% del colore di primo piano |
| [PERCENT_5](#PERCENT-5) | 5% del colore di primo piano. |
| [PERCENT_50](#PERCENT-50) | 50% del colore di primo piano |
| [PERCENT_60](#PERCENT-60) | 60% del colore di primo piano. |
| [PERCENT_70](#PERCENT-70) | 70% del colore di primo piano. |
| [PERCENT_75](#PERCENT-75) | 75% del colore di primo piano. |
| [PERCENT_80](#PERCENT-80) | 80% del colore di primo piano. |
| [PERCENT_90](#PERCENT-90) | 90% del colore di primo piano. |
| [PLAID](#PLAID) | Quadri. |
| [SHINGLE](#SHINGLE) | Scaglie. |
| [SMALL_CHECKER_BOARD](#SMALL-CHECKER-BOARD) | Scacchiera piccola. |
| [SMALL_CONFETTI](#SMALL-CONFETTI) | Confetti piccoli. |
| [SMALL_GRID](#SMALL-GRID) | Piccola griglia. |
| [SOLID_DIAMOND](#SOLID-DIAMOND) | Diamante pieno. |
| [SPHERE](#SPHERE) | Sfera. |
| [TRELLIS](#TRELLIS) | Reticolo. |
| [UPWARD_DIAGONAL](#UPWARD-DIAGONAL) | Diagonale verso l'alto. |
| [VERTICAL](#VERTICAL) | Verticale. |
| [WAVE](#WAVE) | Onda. |
| [WEAVE](#WEAVE) | Intreccio. |
| [WIDE_DOWNWARD_DIAGONAL](#WIDE-DOWNWARD-DIAGONAL) | Diagonale discendente larga. |
| [WIDE_UPWARD_DIAGONAL](#WIDE-UPWARD-DIAGONAL) | Diagonale ascendente larga. |
| [ZIG_ZAG](#ZIG-ZAG) | Zig zag. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String patternTypeName)](#fromName-java.lang.String) |  |
| [getName(int patternType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int patternType)](#toString-int) |  |
### CROSS {#CROSS}
```
public static int CROSS
```


Croce.

### DARK_DOWNWARD_DIAGONAL {#DARK-DOWNWARD-DIAGONAL}
```
public static int DARK_DOWNWARD_DIAGONAL
```


Diagonale discendente scura.

### DARK_HORIZONTAL {#DARK-HORIZONTAL}
```
public static int DARK_HORIZONTAL
```


Orizzontale scura.

### DARK_UPWARD_DIAGONAL {#DARK-UPWARD-DIAGONAL}
```
public static int DARK_UPWARD_DIAGONAL
```


Diagonale ascendente scura.

### DARK_VERTICAL {#DARK-VERTICAL}
```
public static int DARK_VERTICAL
```


Verticale scura.

### DASHED_DOWNWARD_DIAGONAL {#DASHED-DOWNWARD-DIAGONAL}
```
public static int DASHED_DOWNWARD_DIAGONAL
```


Diagonale discendente tratteggiata.

### DASHED_HORIZONTAL {#DASHED-HORIZONTAL}
```
public static int DASHED_HORIZONTAL
```


Orizzontale tratteggiata.

### DASHED_UPWARD_DIAGONAL {#DASHED-UPWARD-DIAGONAL}
```
public static int DASHED_UPWARD_DIAGONAL
```


Diagonale ascendente tratteggiata.

### DASHED_VERTICAL {#DASHED-VERTICAL}
```
public static int DASHED_VERTICAL
```


Verticale tratteggiata.

### DIAGONAL_BRICK {#DIAGONAL-BRICK}
```
public static int DIAGONAL_BRICK
```


Mattone diagonale.

### DIAGONAL_CROSS {#DIAGONAL-CROSS}
```
public static int DIAGONAL_CROSS
```


Croce diagonale.

### DIVOT {#DIVOT}
```
public static int DIVOT
```


Incavatura del modello.

### DOTTED_DIAMOND {#DOTTED-DIAMOND}
```
public static int DOTTED_DIAMOND
```


Diamante punteggiato.

### DOTTED_GRID {#DOTTED-GRID}
```
public static int DOTTED_GRID
```


Griglia punteggiata.

### DOWNWARD_DIAGONAL {#DOWNWARD-DIAGONAL}
```
public static int DOWNWARD_DIAGONAL
```


Diagonale discendente.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Orizzontale.

### HORIZONTAL_BRICK {#HORIZONTAL-BRICK}
```
public static int HORIZONTAL_BRICK
```


Mattone orizzontale.

### LARGE_CHECKER_BOARD {#LARGE-CHECKER-BOARD}
```
public static int LARGE_CHECKER_BOARD
```


Grande scacchiera.

### LARGE_CONFETTI {#LARGE-CONFETTI}
```
public static int LARGE_CONFETTI
```


Grande confetti.

### LARGE_GRID {#LARGE-GRID}
```
public static int LARGE_GRID
```


Griglia grande.

### LIGHT_DOWNWARD_DIAGONAL {#LIGHT-DOWNWARD-DIAGONAL}
```
public static int LIGHT_DOWNWARD_DIAGONAL
```


Diagonale leggera verso il basso.

### LIGHT_HORIZONTAL {#LIGHT-HORIZONTAL}
```
public static int LIGHT_HORIZONTAL
```


Orizzontale leggera.

### LIGHT_UPWARD_DIAGONAL {#LIGHT-UPWARD-DIAGONAL}
```
public static int LIGHT_UPWARD_DIAGONAL
```


Diagonale leggera verso l'alto.

### LIGHT_VERTICAL {#LIGHT-VERTICAL}
```
public static int LIGHT_VERTICAL
```


Verticale leggera.

### NARROW_HORIZONTAL {#NARROW-HORIZONTAL}
```
public static int NARROW_HORIZONTAL
```


Orizzontale stretta.

### NARROW_VERTICAL {#NARROW-VERTICAL}
```
public static int NARROW_VERTICAL
```


Verticale stretta.

### NONE {#NONE}
```
public static int NONE
```


Nessun motivo.

### OUTLINED_DIAMOND {#OUTLINED-DIAMOND}
```
public static int OUTLINED_DIAMOND
```


Diamante contornato.

### PERCENT_10 {#PERCENT-10}
```
public static int PERCENT_10
```


10% del colore di primo piano.

### PERCENT_20 {#PERCENT-20}
```
public static int PERCENT_20
```


20% del colore di primo piano.

### PERCENT_25 {#PERCENT-25}
```
public static int PERCENT_25
```


25% del colore di primo piano.

### PERCENT_30 {#PERCENT-30}
```
public static int PERCENT_30
```


30% del colore di primo piano.

### PERCENT_40 {#PERCENT-40}
```
public static int PERCENT_40
```


40% del colore di primo piano

### PERCENT_5 {#PERCENT-5}
```
public static int PERCENT_5
```


5% del colore di primo piano.

### PERCENT_50 {#PERCENT-50}
```
public static int PERCENT_50
```


50% del colore di primo piano

### PERCENT_60 {#PERCENT-60}
```
public static int PERCENT_60
```


60% del colore di primo piano.

### PERCENT_70 {#PERCENT-70}
```
public static int PERCENT_70
```


70% del colore di primo piano.

### PERCENT_75 {#PERCENT-75}
```
public static int PERCENT_75
```


75% del colore di primo piano.

### PERCENT_80 {#PERCENT-80}
```
public static int PERCENT_80
```


80% del colore di primo piano.

### PERCENT_90 {#PERCENT-90}
```
public static int PERCENT_90
```


90% del colore di primo piano.

### PLAID {#PLAID}
```
public static int PLAID
```


Quadri.

### SHINGLE {#SHINGLE}
```
public static int SHINGLE
```


Scaglie.

### SMALL_CHECKER_BOARD {#SMALL-CHECKER-BOARD}
```
public static int SMALL_CHECKER_BOARD
```


Scacchiera piccola.

### SMALL_CONFETTI {#SMALL-CONFETTI}
```
public static int SMALL_CONFETTI
```


Confetti piccoli.

### SMALL_GRID {#SMALL-GRID}
```
public static int SMALL_GRID
```


Piccola griglia.

### SOLID_DIAMOND {#SOLID-DIAMOND}
```
public static int SOLID_DIAMOND
```


Diamante pieno.

### SPHERE {#SPHERE}
```
public static int SPHERE
```


Sfera.

### TRELLIS {#TRELLIS}
```
public static int TRELLIS
```


Reticolo.

### UPWARD_DIAGONAL {#UPWARD-DIAGONAL}
```
public static int UPWARD_DIAGONAL
```


Diagonale verso l'alto.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Verticale.

### WAVE {#WAVE}
```
public static int WAVE
```


Onda.

### WEAVE {#WEAVE}
```
public static int WEAVE
```


Intreccio.

### WIDE_DOWNWARD_DIAGONAL {#WIDE-DOWNWARD-DIAGONAL}
```
public static int WIDE_DOWNWARD_DIAGONAL
```


Diagonale discendente larga.

### WIDE_UPWARD_DIAGONAL {#WIDE-UPWARD-DIAGONAL}
```
public static int WIDE_UPWARD_DIAGONAL
```


Diagonale ascendente larga.

### ZIG_ZAG {#ZIG-ZAG}
```
public static int ZIG_ZAG
```


Zig zag.

### length {#length}
```
public static int length
```


### fromName(String patternTypeName) {#fromName-java.lang.String}
```
public static int fromName(String patternTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| patternTypeName | java.lang.String |  |

**Returns:**
int
### getName(int patternType) {#getName-int}
```
public static String getName(int patternType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| patternType | int |  |

**Returns:**
java.lang.String
