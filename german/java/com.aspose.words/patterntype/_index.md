---
title: "PatternType"
linktitle: "PatternType"
second_title: "Aspose.Words für Java"
description: "Gibt das Füllmuster an, das zum Ausfüllen einer Form in Java verwendet werden soll."
type: docs
weight: 526
url: /de/java/com.aspose.words/patterntype/
---

**Inheritance:**
java.lang.Object
```
public class PatternType
```

Gibt das Füllmuster an, das zum Ausfüllen einer Form verwendet werden soll.

 **Examples:** 

Zeigt, wie man ein Muster für eine Form festlegt.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CROSS](#CROSS) | Kreuz. |
| [DARK_DOWNWARD_DIAGONAL](#DARK-DOWNWARD-DIAGONAL) | Dunkle abwärts gerichtete Diagonale. |
| [DARK_HORIZONTAL](#DARK-HORIZONTAL) | Dunkle horizontale. |
| [DARK_UPWARD_DIAGONAL](#DARK-UPWARD-DIAGONAL) | Dunkle aufwärts gerichtete Diagonale. |
| [DARK_VERTICAL](#DARK-VERTICAL) | Dunkle vertikale. |
| [DASHED_DOWNWARD_DIAGONAL](#DASHED-DOWNWARD-DIAGONAL) | Gestrichelte abwärts gerichtete Diagonale. |
| [DASHED_HORIZONTAL](#DASHED-HORIZONTAL) | Gestrichelte horizontale. |
| [DASHED_UPWARD_DIAGONAL](#DASHED-UPWARD-DIAGONAL) | Gestrichelte aufwärts gerichtete Diagonale. |
| [DASHED_VERTICAL](#DASHED-VERTICAL) | Gestrichelte vertikale. |
| [DIAGONAL_BRICK](#DIAGONAL-BRICK) | Diagonale Ziegel. |
| [DIAGONAL_CROSS](#DIAGONAL-CROSS) | Diagonales Kreuz. |
| [DIVOT](#DIVOT) | Mustervertiefung. |
| [DOTTED_DIAMOND](#DOTTED-DIAMOND) | Gepunkteter Diamant. |
| [DOTTED_GRID](#DOTTED-GRID) | Gepunktetes Raster. |
| [DOWNWARD_DIAGONAL](#DOWNWARD-DIAGONAL) | Abwärts gerichtete Diagonale. |
| [HORIZONTAL](#HORIZONTAL) | Horizontal. |
| [HORIZONTAL_BRICK](#HORIZONTAL-BRICK) | Horizontale Ziegel. |
| [LARGE_CHECKER_BOARD](#LARGE-CHECKER-BOARD) | Großes Schachbrett. |
| [LARGE_CONFETTI](#LARGE-CONFETTI) | Großes Konfetti. |
| [LARGE_GRID](#LARGE-GRID) | Großes Raster. |
| [LIGHT_DOWNWARD_DIAGONAL](#LIGHT-DOWNWARD-DIAGONAL) | Helle abwärts gerichtete Diagonale. |
| [LIGHT_HORIZONTAL](#LIGHT-HORIZONTAL) | Leicht horizontal. |
| [LIGHT_UPWARD_DIAGONAL](#LIGHT-UPWARD-DIAGONAL) | Leicht diagonal nach oben. |
| [LIGHT_VERTICAL](#LIGHT-VERTICAL) | Leicht vertikal. |
| [NARROW_HORIZONTAL](#NARROW-HORIZONTAL) | Schmal horizontal. |
| [NARROW_VERTICAL](#NARROW-VERTICAL) | Schmal vertikal. |
| [NONE](#NONE) | Kein Muster. |
| [OUTLINED_DIAMOND](#OUTLINED-DIAMOND) | Umrandeter Diamant. |
| [PERCENT_10](#PERCENT-10) | 10% der Vordergrundfarbe. |
| [PERCENT_20](#PERCENT-20) | 20% der Vordergrundfarbe. |
| [PERCENT_25](#PERCENT-25) | 25% der Vordergrundfarbe. |
| [PERCENT_30](#PERCENT-30) | 30% der Vordergrundfarbe. |
| [PERCENT_40](#PERCENT-40) | 40% der Vordergrundfarbe |
| [PERCENT_5](#PERCENT-5) | 5% der Vordergrundfarbe. |
| [PERCENT_50](#PERCENT-50) | 50% der Vordergrundfarbe |
| [PERCENT_60](#PERCENT-60) | 60% der Vordergrundfarbe. |
| [PERCENT_70](#PERCENT-70) | 70% der Vordergrundfarbe. |
| [PERCENT_75](#PERCENT-75) | 75% der Vordergrundfarbe. |
| [PERCENT_80](#PERCENT-80) | 80% der Vordergrundfarbe. |
| [PERCENT_90](#PERCENT-90) | 90% der Vordergrundfarbe. |
| [PLAID](#PLAID) | Kariert. |
| [SHINGLE](#SHINGLE) | Schindel. |
| [SMALL_CHECKER_BOARD](#SMALL-CHECKER-BOARD) | Kleines Schachbrett. |
| [SMALL_CONFETTI](#SMALL-CONFETTI) | Kleines Konfetti. |
| [SMALL_GRID](#SMALL-GRID) | Kleines Raster. |
| [SOLID_DIAMOND](#SOLID-DIAMOND) | Gefüllter Diamant. |
| [SPHERE](#SPHERE) | Kugel. |
| [TRELLIS](#TRELLIS) | Spalier. |
| [UPWARD_DIAGONAL](#UPWARD-DIAGONAL) | Aufsteigende Diagonale. |
| [VERTICAL](#VERTICAL) | Vertikal. |
| [WAVE](#WAVE) | Welle. |
| [WEAVE](#WEAVE) | Weben. |
| [WIDE_DOWNWARD_DIAGONAL](#WIDE-DOWNWARD-DIAGONAL) | Breite abwärts gerichtete Diagonale. |
| [WIDE_UPWARD_DIAGONAL](#WIDE-UPWARD-DIAGONAL) | Breite aufwärts gerichtete Diagonale. |
| [ZIG_ZAG](#ZIG-ZAG) | Zickzack. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String patternTypeName)](#fromName-java.lang.String) |  |
| [getName(int patternType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int patternType)](#toString-int) |  |
### CROSS {#CROSS}
```
public static int CROSS
```


Kreuz.

### DARK_DOWNWARD_DIAGONAL {#DARK-DOWNWARD-DIAGONAL}
```
public static int DARK_DOWNWARD_DIAGONAL
```


Dunkle abwärts gerichtete Diagonale.

### DARK_HORIZONTAL {#DARK-HORIZONTAL}
```
public static int DARK_HORIZONTAL
```


Dunkle horizontale.

### DARK_UPWARD_DIAGONAL {#DARK-UPWARD-DIAGONAL}
```
public static int DARK_UPWARD_DIAGONAL
```


Dunkle aufwärts gerichtete Diagonale.

### DARK_VERTICAL {#DARK-VERTICAL}
```
public static int DARK_VERTICAL
```


Dunkle vertikale.

### DASHED_DOWNWARD_DIAGONAL {#DASHED-DOWNWARD-DIAGONAL}
```
public static int DASHED_DOWNWARD_DIAGONAL
```


Gestrichelte abwärts gerichtete Diagonale.

### DASHED_HORIZONTAL {#DASHED-HORIZONTAL}
```
public static int DASHED_HORIZONTAL
```


Gestrichelte horizontale.

### DASHED_UPWARD_DIAGONAL {#DASHED-UPWARD-DIAGONAL}
```
public static int DASHED_UPWARD_DIAGONAL
```


Gestrichelte aufwärts gerichtete Diagonale.

### DASHED_VERTICAL {#DASHED-VERTICAL}
```
public static int DASHED_VERTICAL
```


Gestrichelte vertikale.

### DIAGONAL_BRICK {#DIAGONAL-BRICK}
```
public static int DIAGONAL_BRICK
```


Diagonale Ziegel.

### DIAGONAL_CROSS {#DIAGONAL-CROSS}
```
public static int DIAGONAL_CROSS
```


Diagonales Kreuz.

### DIVOT {#DIVOT}
```
public static int DIVOT
```


Mustervertiefung.

### DOTTED_DIAMOND {#DOTTED-DIAMOND}
```
public static int DOTTED_DIAMOND
```


Gepunkteter Diamant.

### DOTTED_GRID {#DOTTED-GRID}
```
public static int DOTTED_GRID
```


Gepunktetes Raster.

### DOWNWARD_DIAGONAL {#DOWNWARD-DIAGONAL}
```
public static int DOWNWARD_DIAGONAL
```


Abwärts gerichtete Diagonale.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Horizontal.

### HORIZONTAL_BRICK {#HORIZONTAL-BRICK}
```
public static int HORIZONTAL_BRICK
```


Horizontale Ziegel.

### LARGE_CHECKER_BOARD {#LARGE-CHECKER-BOARD}
```
public static int LARGE_CHECKER_BOARD
```


Großes Schachbrett.

### LARGE_CONFETTI {#LARGE-CONFETTI}
```
public static int LARGE_CONFETTI
```


Großes Konfetti.

### LARGE_GRID {#LARGE-GRID}
```
public static int LARGE_GRID
```


Großes Raster.

### LIGHT_DOWNWARD_DIAGONAL {#LIGHT-DOWNWARD-DIAGONAL}
```
public static int LIGHT_DOWNWARD_DIAGONAL
```


Helle abwärts gerichtete Diagonale.

### LIGHT_HORIZONTAL {#LIGHT-HORIZONTAL}
```
public static int LIGHT_HORIZONTAL
```


Leicht horizontal.

### LIGHT_UPWARD_DIAGONAL {#LIGHT-UPWARD-DIAGONAL}
```
public static int LIGHT_UPWARD_DIAGONAL
```


Leicht diagonal nach oben.

### LIGHT_VERTICAL {#LIGHT-VERTICAL}
```
public static int LIGHT_VERTICAL
```


Leicht vertikal.

### NARROW_HORIZONTAL {#NARROW-HORIZONTAL}
```
public static int NARROW_HORIZONTAL
```


Schmal horizontal.

### NARROW_VERTICAL {#NARROW-VERTICAL}
```
public static int NARROW_VERTICAL
```


Schmal vertikal.

### NONE {#NONE}
```
public static int NONE
```


Kein Muster.

### OUTLINED_DIAMOND {#OUTLINED-DIAMOND}
```
public static int OUTLINED_DIAMOND
```


Umrandeter Diamant.

### PERCENT_10 {#PERCENT-10}
```
public static int PERCENT_10
```


10% der Vordergrundfarbe.

### PERCENT_20 {#PERCENT-20}
```
public static int PERCENT_20
```


20% der Vordergrundfarbe.

### PERCENT_25 {#PERCENT-25}
```
public static int PERCENT_25
```


25% der Vordergrundfarbe.

### PERCENT_30 {#PERCENT-30}
```
public static int PERCENT_30
```


30% der Vordergrundfarbe.

### PERCENT_40 {#PERCENT-40}
```
public static int PERCENT_40
```


40% der Vordergrundfarbe

### PERCENT_5 {#PERCENT-5}
```
public static int PERCENT_5
```


5% der Vordergrundfarbe.

### PERCENT_50 {#PERCENT-50}
```
public static int PERCENT_50
```


50% der Vordergrundfarbe

### PERCENT_60 {#PERCENT-60}
```
public static int PERCENT_60
```


60% der Vordergrundfarbe.

### PERCENT_70 {#PERCENT-70}
```
public static int PERCENT_70
```


70% der Vordergrundfarbe.

### PERCENT_75 {#PERCENT-75}
```
public static int PERCENT_75
```


75% der Vordergrundfarbe.

### PERCENT_80 {#PERCENT-80}
```
public static int PERCENT_80
```


80% der Vordergrundfarbe.

### PERCENT_90 {#PERCENT-90}
```
public static int PERCENT_90
```


90% der Vordergrundfarbe.

### PLAID {#PLAID}
```
public static int PLAID
```


Kariert.

### SHINGLE {#SHINGLE}
```
public static int SHINGLE
```


Schindel.

### SMALL_CHECKER_BOARD {#SMALL-CHECKER-BOARD}
```
public static int SMALL_CHECKER_BOARD
```


Kleines Schachbrett.

### SMALL_CONFETTI {#SMALL-CONFETTI}
```
public static int SMALL_CONFETTI
```


Kleines Konfetti.

### SMALL_GRID {#SMALL-GRID}
```
public static int SMALL_GRID
```


Kleines Raster.

### SOLID_DIAMOND {#SOLID-DIAMOND}
```
public static int SOLID_DIAMOND
```


Gefüllter Diamant.

### SPHERE {#SPHERE}
```
public static int SPHERE
```


Kugel.

### TRELLIS {#TRELLIS}
```
public static int TRELLIS
```


Spalier.

### UPWARD_DIAGONAL {#UPWARD-DIAGONAL}
```
public static int UPWARD_DIAGONAL
```


Aufsteigende Diagonale.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Vertikal.

### WAVE {#WAVE}
```
public static int WAVE
```


Welle.

### WEAVE {#WEAVE}
```
public static int WEAVE
```


Weben.

### WIDE_DOWNWARD_DIAGONAL {#WIDE-DOWNWARD-DIAGONAL}
```
public static int WIDE_DOWNWARD_DIAGONAL
```


Breite abwärts gerichtete Diagonale.

### WIDE_UPWARD_DIAGONAL {#WIDE-UPWARD-DIAGONAL}
```
public static int WIDE_UPWARD_DIAGONAL
```


Breite aufwärts gerichtete Diagonale.

### ZIG_ZAG {#ZIG-ZAG}
```
public static int ZIG_ZAG
```


Zickzack.

### length {#length}
```
public static int length
```


### fromName(String patternTypeName) {#fromName-java.lang.String}
```
public static int fromName(String patternTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| patternTypeName | java.lang.String |  |

**Returns:**
int
### getName(int patternType) {#getName-int}
```
public static String getName(int patternType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| MusterTyp | int |  |

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| MusterTyp | int |  |

**Returns:**
java.lang.String
