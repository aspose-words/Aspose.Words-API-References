---
title: PatternType
linktitle: PatternType
second_title: Aspose.Words for Java
description: Specifies the fill pattern to be used to fill a shape in Java.
type: docs
weight: 507
url: /java/com.aspose.words/patterntype/
---

**Inheritance:**
java.lang.Object
```
public class PatternType
```

Specifies the fill pattern to be used to fill a shape.

 **Examples:** 

Shows how to set pattern for a shape.

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
## Fields

| Field | Description |
| --- | --- |
| [CROSS](#CROSS) | Cross. |
| [DARK_DOWNWARD_DIAGONAL](#DARK-DOWNWARD-DIAGONAL) | Dark downward diagonal. |
| [DARK_HORIZONTAL](#DARK-HORIZONTAL) | Dark horizontal. |
| [DARK_UPWARD_DIAGONAL](#DARK-UPWARD-DIAGONAL) | Dark upward diagonal. |
| [DARK_VERTICAL](#DARK-VERTICAL) | Dark vertical. |
| [DASHED_DOWNWARD_DIAGONAL](#DASHED-DOWNWARD-DIAGONAL) | Dashed downward diagonal. |
| [DASHED_HORIZONTAL](#DASHED-HORIZONTAL) | Dashed horizontal. |
| [DASHED_UPWARD_DIAGONAL](#DASHED-UPWARD-DIAGONAL) | Dashed upward diagonal. |
| [DASHED_VERTICAL](#DASHED-VERTICAL) | Dashed vertical. |
| [DIAGONAL_BRICK](#DIAGONAL-BRICK) | Diagonal brick. |
| [DIAGONAL_CROSS](#DIAGONAL-CROSS) | Diagonal cross. |
| [DIVOT](#DIVOT) | Pattern divot. |
| [DOTTED_DIAMOND](#DOTTED-DIAMOND) | Dotted diamond. |
| [DOTTED_GRID](#DOTTED-GRID) | Dotted grid. |
| [DOWNWARD_DIAGONAL](#DOWNWARD-DIAGONAL) | Downward diagonal. |
| [HORIZONTAL](#HORIZONTAL) | Horizontal. |
| [HORIZONTAL_BRICK](#HORIZONTAL-BRICK) | Horizontal brick. |
| [LARGE_CHECKER_BOARD](#LARGE-CHECKER-BOARD) | Large checker board. |
| [LARGE_CONFETTI](#LARGE-CONFETTI) | Large confetti. |
| [LARGE_GRID](#LARGE-GRID) | Large grid. |
| [LIGHT_DOWNWARD_DIAGONAL](#LIGHT-DOWNWARD-DIAGONAL) | Light downward diagonal. |
| [LIGHT_HORIZONTAL](#LIGHT-HORIZONTAL) | Light horizontal. |
| [LIGHT_UPWARD_DIAGONAL](#LIGHT-UPWARD-DIAGONAL) | Light upward diagonal. |
| [LIGHT_VERTICAL](#LIGHT-VERTICAL) | Light vertical. |
| [NARROW_HORIZONTAL](#NARROW-HORIZONTAL) | Narrow horizontal. |
| [NARROW_VERTICAL](#NARROW-VERTICAL) | Narrow vertical. |
| [NONE](#NONE) | No pattern. |
| [OUTLINED_DIAMOND](#OUTLINED-DIAMOND) | Outlined diamond. |
| [PERCENT_10](#PERCENT-10) | 10% of the foreground color. |
| [PERCENT_20](#PERCENT-20) | 20% of the foreground color. |
| [PERCENT_25](#PERCENT-25) | 25% of the foreground color. |
| [PERCENT_30](#PERCENT-30) | 30% of the foreground color. |
| [PERCENT_40](#PERCENT-40) | 40% of the foreground color |
| [PERCENT_5](#PERCENT-5) | 5% of the foreground color. |
| [PERCENT_50](#PERCENT-50) | 50% of the foreground color |
| [PERCENT_60](#PERCENT-60) | 60% of the foreground color. |
| [PERCENT_70](#PERCENT-70) | 70% of the foreground color. |
| [PERCENT_75](#PERCENT-75) | 75% of the foreground color. |
| [PERCENT_80](#PERCENT-80) | 80% of the foreground color. |
| [PERCENT_90](#PERCENT-90) | 90% of the foreground color. |
| [PLAID](#PLAID) | Plaid. |
| [SHINGLE](#SHINGLE) | Shingle. |
| [SMALL_CHECKER_BOARD](#SMALL-CHECKER-BOARD) | Small checker board. |
| [SMALL_CONFETTI](#SMALL-CONFETTI) | Small confetti. |
| [SMALL_GRID](#SMALL-GRID) | Small grid. |
| [SOLID_DIAMOND](#SOLID-DIAMOND) | Solid diamond. |
| [SPHERE](#SPHERE) | Sphere. |
| [TRELLIS](#TRELLIS) | Trellis. |
| [UPWARD_DIAGONAL](#UPWARD-DIAGONAL) | Upward diagonal. |
| [VERTICAL](#VERTICAL) | Vertical. |
| [WAVE](#WAVE) | Wave. |
| [WEAVE](#WEAVE) | Weave. |
| [WIDE_DOWNWARD_DIAGONAL](#WIDE-DOWNWARD-DIAGONAL) | Wide downward diagonal. |
| [WIDE_UPWARD_DIAGONAL](#WIDE-UPWARD-DIAGONAL) | Wide upward diagonal. |
| [ZIG_ZAG](#ZIG-ZAG) | Zig zag. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String patternTypeName)](#fromName-java.lang.String) |  |
| [getName(int patternType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int patternType)](#toString-int) |  |
### CROSS {#CROSS}
```
public static int CROSS
```


Cross.

### DARK_DOWNWARD_DIAGONAL {#DARK-DOWNWARD-DIAGONAL}
```
public static int DARK_DOWNWARD_DIAGONAL
```


Dark downward diagonal.

### DARK_HORIZONTAL {#DARK-HORIZONTAL}
```
public static int DARK_HORIZONTAL
```


Dark horizontal.

### DARK_UPWARD_DIAGONAL {#DARK-UPWARD-DIAGONAL}
```
public static int DARK_UPWARD_DIAGONAL
```


Dark upward diagonal.

### DARK_VERTICAL {#DARK-VERTICAL}
```
public static int DARK_VERTICAL
```


Dark vertical.

### DASHED_DOWNWARD_DIAGONAL {#DASHED-DOWNWARD-DIAGONAL}
```
public static int DASHED_DOWNWARD_DIAGONAL
```


Dashed downward diagonal.

### DASHED_HORIZONTAL {#DASHED-HORIZONTAL}
```
public static int DASHED_HORIZONTAL
```


Dashed horizontal.

### DASHED_UPWARD_DIAGONAL {#DASHED-UPWARD-DIAGONAL}
```
public static int DASHED_UPWARD_DIAGONAL
```


Dashed upward diagonal.

### DASHED_VERTICAL {#DASHED-VERTICAL}
```
public static int DASHED_VERTICAL
```


Dashed vertical.

### DIAGONAL_BRICK {#DIAGONAL-BRICK}
```
public static int DIAGONAL_BRICK
```


Diagonal brick.

### DIAGONAL_CROSS {#DIAGONAL-CROSS}
```
public static int DIAGONAL_CROSS
```


Diagonal cross.

### DIVOT {#DIVOT}
```
public static int DIVOT
```


Pattern divot.

### DOTTED_DIAMOND {#DOTTED-DIAMOND}
```
public static int DOTTED_DIAMOND
```


Dotted diamond.

### DOTTED_GRID {#DOTTED-GRID}
```
public static int DOTTED_GRID
```


Dotted grid.

### DOWNWARD_DIAGONAL {#DOWNWARD-DIAGONAL}
```
public static int DOWNWARD_DIAGONAL
```


Downward diagonal.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Horizontal.

### HORIZONTAL_BRICK {#HORIZONTAL-BRICK}
```
public static int HORIZONTAL_BRICK
```


Horizontal brick.

### LARGE_CHECKER_BOARD {#LARGE-CHECKER-BOARD}
```
public static int LARGE_CHECKER_BOARD
```


Large checker board.

### LARGE_CONFETTI {#LARGE-CONFETTI}
```
public static int LARGE_CONFETTI
```


Large confetti.

### LARGE_GRID {#LARGE-GRID}
```
public static int LARGE_GRID
```


Large grid.

### LIGHT_DOWNWARD_DIAGONAL {#LIGHT-DOWNWARD-DIAGONAL}
```
public static int LIGHT_DOWNWARD_DIAGONAL
```


Light downward diagonal.

### LIGHT_HORIZONTAL {#LIGHT-HORIZONTAL}
```
public static int LIGHT_HORIZONTAL
```


Light horizontal.

### LIGHT_UPWARD_DIAGONAL {#LIGHT-UPWARD-DIAGONAL}
```
public static int LIGHT_UPWARD_DIAGONAL
```


Light upward diagonal.

### LIGHT_VERTICAL {#LIGHT-VERTICAL}
```
public static int LIGHT_VERTICAL
```


Light vertical.

### NARROW_HORIZONTAL {#NARROW-HORIZONTAL}
```
public static int NARROW_HORIZONTAL
```


Narrow horizontal.

### NARROW_VERTICAL {#NARROW-VERTICAL}
```
public static int NARROW_VERTICAL
```


Narrow vertical.

### NONE {#NONE}
```
public static int NONE
```


No pattern.

### OUTLINED_DIAMOND {#OUTLINED-DIAMOND}
```
public static int OUTLINED_DIAMOND
```


Outlined diamond.

### PERCENT_10 {#PERCENT-10}
```
public static int PERCENT_10
```


10% of the foreground color.

### PERCENT_20 {#PERCENT-20}
```
public static int PERCENT_20
```


20% of the foreground color.

### PERCENT_25 {#PERCENT-25}
```
public static int PERCENT_25
```


25% of the foreground color.

### PERCENT_30 {#PERCENT-30}
```
public static int PERCENT_30
```


30% of the foreground color.

### PERCENT_40 {#PERCENT-40}
```
public static int PERCENT_40
```


40% of the foreground color

### PERCENT_5 {#PERCENT-5}
```
public static int PERCENT_5
```


5% of the foreground color.

### PERCENT_50 {#PERCENT-50}
```
public static int PERCENT_50
```


50% of the foreground color

### PERCENT_60 {#PERCENT-60}
```
public static int PERCENT_60
```


60% of the foreground color.

### PERCENT_70 {#PERCENT-70}
```
public static int PERCENT_70
```


70% of the foreground color.

### PERCENT_75 {#PERCENT-75}
```
public static int PERCENT_75
```


75% of the foreground color.

### PERCENT_80 {#PERCENT-80}
```
public static int PERCENT_80
```


80% of the foreground color.

### PERCENT_90 {#PERCENT-90}
```
public static int PERCENT_90
```


90% of the foreground color.

### PLAID {#PLAID}
```
public static int PLAID
```


Plaid.

### SHINGLE {#SHINGLE}
```
public static int SHINGLE
```


Shingle.

### SMALL_CHECKER_BOARD {#SMALL-CHECKER-BOARD}
```
public static int SMALL_CHECKER_BOARD
```


Small checker board.

### SMALL_CONFETTI {#SMALL-CONFETTI}
```
public static int SMALL_CONFETTI
```


Small confetti.

### SMALL_GRID {#SMALL-GRID}
```
public static int SMALL_GRID
```


Small grid.

### SOLID_DIAMOND {#SOLID-DIAMOND}
```
public static int SOLID_DIAMOND
```


Solid diamond.

### SPHERE {#SPHERE}
```
public static int SPHERE
```


Sphere.

### TRELLIS {#TRELLIS}
```
public static int TRELLIS
```


Trellis.

### UPWARD_DIAGONAL {#UPWARD-DIAGONAL}
```
public static int UPWARD_DIAGONAL
```


Upward diagonal.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Vertical.

### WAVE {#WAVE}
```
public static int WAVE
```


Wave.

### WEAVE {#WEAVE}
```
public static int WEAVE
```


Weave.

### WIDE_DOWNWARD_DIAGONAL {#WIDE-DOWNWARD-DIAGONAL}
```
public static int WIDE_DOWNWARD_DIAGONAL
```


Wide downward diagonal.

### WIDE_UPWARD_DIAGONAL {#WIDE-UPWARD-DIAGONAL}
```
public static int WIDE_UPWARD_DIAGONAL
```


Wide upward diagonal.

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
| Parameter | Type | Description |
| --- | --- | --- |
| patternTypeName | java.lang.String |  |

**Returns:**
int
### getName(int patternType) {#getName-int}
```
public static String getName(int patternType)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| patternType | int |  |

**Returns:**
java.lang.String
