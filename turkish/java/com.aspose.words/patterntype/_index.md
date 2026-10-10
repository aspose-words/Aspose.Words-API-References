---
title: "PatternType"
linktitle: "PatternType"
second_title: "Aspose.Words Java için"
description: "Java'da bir şekli doldurmak için kullanılacak dolgu desenini belirtir."
type: docs
weight: 526
url: /tr/java/com.aspose.words/patterntype/
---

**Inheritance:**
java.lang.Object
```
public class PatternType
```

Bir şekli doldurmak için kullanılacak dolgu desenini belirtir.

 **Examples:** 

Bir şekil için desenin nasıl ayarlanacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CROSS](#CROSS) | Çapraz. |
| [DARK_DOWNWARD_DIAGONAL](#DARK-DOWNWARD-DIAGONAL) | Koyu aşağı diyagonal. |
| [DARK_HORIZONTAL](#DARK-HORIZONTAL) | Koyu yatay. |
| [DARK_UPWARD_DIAGONAL](#DARK-UPWARD-DIAGONAL) | Koyu yukarı diyagonal. |
| [DARK_VERTICAL](#DARK-VERTICAL) | Koyu dikey. |
| [DASHED_DOWNWARD_DIAGONAL](#DASHED-DOWNWARD-DIAGONAL) | Kesikli aşağı diyagonal. |
| [DASHED_HORIZONTAL](#DASHED-HORIZONTAL) | Kesikli yatay. |
| [DASHED_UPWARD_DIAGONAL](#DASHED-UPWARD-DIAGONAL) | Kesikli yukarı diyagonal. |
| [DASHED_VERTICAL](#DASHED-VERTICAL) | Kesikli dikey. |
| [DIAGONAL_BRICK](#DIAGONAL-BRICK) | Diyagonal tuğla. |
| [DIAGONAL_CROSS](#DIAGONAL-CROSS) | Diyagonal çapraz. |
| [DIVOT](#DIVOT) | Desen çöküntüsü. |
| [DOTTED_DIAMOND](#DOTTED-DIAMOND) | Noktalı elmas. |
| [DOTTED_GRID](#DOTTED-GRID) | Noktalı ızgara. |
| [DOWNWARD_DIAGONAL](#DOWNWARD-DIAGONAL) | Aşağı diyagonal. |
| [HORIZONTAL](#HORIZONTAL) | Yatay. |
| [HORIZONTAL_BRICK](#HORIZONTAL-BRICK) | Yatay tuğla. |
| [LARGE_CHECKER_BOARD](#LARGE-CHECKER-BOARD) | Büyük dama tahtası. |
| [LARGE_CONFETTI](#LARGE-CONFETTI) | Büyük konfeti. |
| [LARGE_GRID](#LARGE-GRID) | Büyük ızgara. |
| [LIGHT_DOWNWARD_DIAGONAL](#LIGHT-DOWNWARD-DIAGONAL) | Açık aşağı diyagonal. |
| [LIGHT_HORIZONTAL](#LIGHT-HORIZONTAL) | Açık yatay. |
| [LIGHT_UPWARD_DIAGONAL](#LIGHT-UPWARD-DIAGONAL) | Açık yukarı diyagonal. |
| [LIGHT_VERTICAL](#LIGHT-VERTICAL) | Açık dikey. |
| [NARROW_HORIZONTAL](#NARROW-HORIZONTAL) | Dar yatay. |
| [NARROW_VERTICAL](#NARROW-VERTICAL) | Dar dikey. |
| [NONE](#NONE) | Desen yok. |
| [OUTLINED_DIAMOND](#OUTLINED-DIAMOND) | Konturlu elmas. |
| [PERCENT_10](#PERCENT-10) | Ön plan renginin %10'u. |
| [PERCENT_20](#PERCENT-20) | Ön plan renginin %20'si. |
| [PERCENT_25](#PERCENT-25) | Ön plan renginin %25'i. |
| [PERCENT_30](#PERCENT-30) | Ön plan renginin %30'u. |
| [PERCENT_40](#PERCENT-40) | Ön plan renginin %40'ı |
| [PERCENT_5](#PERCENT-5) | Ön plan renginin %5'i. |
| [PERCENT_50](#PERCENT-50) | Ön plan renginin %50'si |
| [PERCENT_60](#PERCENT-60) | Ön plan renginin %60'ı. |
| [PERCENT_70](#PERCENT-70) | Ön plan renginin %70'i. |
| [PERCENT_75](#PERCENT-75) | Ön plan renginin %75'i. |
| [PERCENT_80](#PERCENT-80) | Ön plan renginin %80'i. |
| [PERCENT_90](#PERCENT-90) | Ön plan renginin %90'ı. |
| [PLAID](#PLAID) | Kareli. |
| [SHINGLE](#SHINGLE) | Şingıl. |
| [SMALL_CHECKER_BOARD](#SMALL-CHECKER-BOARD) | Küçük dama tahtası. |
| [SMALL_CONFETTI](#SMALL-CONFETTI) | Küçük konfeti. |
| [SMALL_GRID](#SMALL-GRID) | Küçük ızgara. |
| [SOLID_DIAMOND](#SOLID-DIAMOND) | Katı elmas. |
| [SPHERE](#SPHERE) | Küre. |
| [TRELLIS](#TRELLIS) | Kafes. |
| [UPWARD_DIAGONAL](#UPWARD-DIAGONAL) | Yukarı doğru diyagonal. |
| [VERTICAL](#VERTICAL) | Dikey. |
| [WAVE](#WAVE) | Dalga. |
| [WEAVE](#WEAVE) | Dokuma. |
| [WIDE_DOWNWARD_DIAGONAL](#WIDE-DOWNWARD-DIAGONAL) | Geniş aşağı doğru diyagonal. |
| [WIDE_UPWARD_DIAGONAL](#WIDE-UPWARD-DIAGONAL) | Geniş yukarı doğru diyagonal. |
| [ZIG_ZAG](#ZIG-ZAG) | Zikzak. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String patternTypeName)](#fromName-java.lang.String) |  |
| [getName(int patternType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int patternType)](#toString-int) |  |
### CROSS {#CROSS}
```
public static int CROSS
```


Çapraz.

### DARK_DOWNWARD_DIAGONAL {#DARK-DOWNWARD-DIAGONAL}
```
public static int DARK_DOWNWARD_DIAGONAL
```


Koyu aşağı diyagonal.

### DARK_HORIZONTAL {#DARK-HORIZONTAL}
```
public static int DARK_HORIZONTAL
```


Koyu yatay.

### DARK_UPWARD_DIAGONAL {#DARK-UPWARD-DIAGONAL}
```
public static int DARK_UPWARD_DIAGONAL
```


Koyu yukarı diyagonal.

### DARK_VERTICAL {#DARK-VERTICAL}
```
public static int DARK_VERTICAL
```


Koyu dikey.

### DASHED_DOWNWARD_DIAGONAL {#DASHED-DOWNWARD-DIAGONAL}
```
public static int DASHED_DOWNWARD_DIAGONAL
```


Kesikli aşağı diyagonal.

### DASHED_HORIZONTAL {#DASHED-HORIZONTAL}
```
public static int DASHED_HORIZONTAL
```


Kesikli yatay.

### DASHED_UPWARD_DIAGONAL {#DASHED-UPWARD-DIAGONAL}
```
public static int DASHED_UPWARD_DIAGONAL
```


Kesikli yukarı diyagonal.

### DASHED_VERTICAL {#DASHED-VERTICAL}
```
public static int DASHED_VERTICAL
```


Kesikli dikey.

### DIAGONAL_BRICK {#DIAGONAL-BRICK}
```
public static int DIAGONAL_BRICK
```


Diyagonal tuğla.

### DIAGONAL_CROSS {#DIAGONAL-CROSS}
```
public static int DIAGONAL_CROSS
```


Diyagonal çapraz.

### DIVOT {#DIVOT}
```
public static int DIVOT
```


Desen çöküntüsü.

### DOTTED_DIAMOND {#DOTTED-DIAMOND}
```
public static int DOTTED_DIAMOND
```


Noktalı elmas.

### DOTTED_GRID {#DOTTED-GRID}
```
public static int DOTTED_GRID
```


Noktalı ızgara.

### DOWNWARD_DIAGONAL {#DOWNWARD-DIAGONAL}
```
public static int DOWNWARD_DIAGONAL
```


Aşağı diyagonal.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Yatay.

### HORIZONTAL_BRICK {#HORIZONTAL-BRICK}
```
public static int HORIZONTAL_BRICK
```


Yatay tuğla.

### LARGE_CHECKER_BOARD {#LARGE-CHECKER-BOARD}
```
public static int LARGE_CHECKER_BOARD
```


Büyük dama tahtası.

### LARGE_CONFETTI {#LARGE-CONFETTI}
```
public static int LARGE_CONFETTI
```


Büyük konfeti.

### LARGE_GRID {#LARGE-GRID}
```
public static int LARGE_GRID
```


Büyük ızgara.

### LIGHT_DOWNWARD_DIAGONAL {#LIGHT-DOWNWARD-DIAGONAL}
```
public static int LIGHT_DOWNWARD_DIAGONAL
```


Açık aşağı diyagonal.

### LIGHT_HORIZONTAL {#LIGHT-HORIZONTAL}
```
public static int LIGHT_HORIZONTAL
```


Açık yatay.

### LIGHT_UPWARD_DIAGONAL {#LIGHT-UPWARD-DIAGONAL}
```
public static int LIGHT_UPWARD_DIAGONAL
```


Açık yukarı diyagonal.

### LIGHT_VERTICAL {#LIGHT-VERTICAL}
```
public static int LIGHT_VERTICAL
```


Açık dikey.

### NARROW_HORIZONTAL {#NARROW-HORIZONTAL}
```
public static int NARROW_HORIZONTAL
```


Dar yatay.

### NARROW_VERTICAL {#NARROW-VERTICAL}
```
public static int NARROW_VERTICAL
```


Dar dikey.

### NONE {#NONE}
```
public static int NONE
```


Desen yok.

### OUTLINED_DIAMOND {#OUTLINED-DIAMOND}
```
public static int OUTLINED_DIAMOND
```


Konturlu elmas.

### PERCENT_10 {#PERCENT-10}
```
public static int PERCENT_10
```


Ön plan renginin %10'u.

### PERCENT_20 {#PERCENT-20}
```
public static int PERCENT_20
```


Ön plan renginin %20'si.

### PERCENT_25 {#PERCENT-25}
```
public static int PERCENT_25
```


Ön plan renginin %25'i.

### PERCENT_30 {#PERCENT-30}
```
public static int PERCENT_30
```


Ön plan renginin %30'u.

### PERCENT_40 {#PERCENT-40}
```
public static int PERCENT_40
```


Ön plan renginin %40'ı

### PERCENT_5 {#PERCENT-5}
```
public static int PERCENT_5
```


Ön plan renginin %5'i.

### PERCENT_50 {#PERCENT-50}
```
public static int PERCENT_50
```


Ön plan renginin %50'si

### PERCENT_60 {#PERCENT-60}
```
public static int PERCENT_60
```


Ön plan renginin %60'ı.

### PERCENT_70 {#PERCENT-70}
```
public static int PERCENT_70
```


Ön plan renginin %70'i.

### PERCENT_75 {#PERCENT-75}
```
public static int PERCENT_75
```


Ön plan renginin %75'i.

### PERCENT_80 {#PERCENT-80}
```
public static int PERCENT_80
```


Ön plan renginin %80'i.

### PERCENT_90 {#PERCENT-90}
```
public static int PERCENT_90
```


Ön plan renginin %90'ı.

### PLAID {#PLAID}
```
public static int PLAID
```


Kareli.

### SHINGLE {#SHINGLE}
```
public static int SHINGLE
```


Şingıl.

### SMALL_CHECKER_BOARD {#SMALL-CHECKER-BOARD}
```
public static int SMALL_CHECKER_BOARD
```


Küçük dama tahtası.

### SMALL_CONFETTI {#SMALL-CONFETTI}
```
public static int SMALL_CONFETTI
```


Küçük konfeti.

### SMALL_GRID {#SMALL-GRID}
```
public static int SMALL_GRID
```


Küçük ızgara.

### SOLID_DIAMOND {#SOLID-DIAMOND}
```
public static int SOLID_DIAMOND
```


Katı elmas.

### SPHERE {#SPHERE}
```
public static int SPHERE
```


Küre.

### TRELLIS {#TRELLIS}
```
public static int TRELLIS
```


Kafes.

### UPWARD_DIAGONAL {#UPWARD-DIAGONAL}
```
public static int UPWARD_DIAGONAL
```


Yukarı doğru diyagonal.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Dikey.

### WAVE {#WAVE}
```
public static int WAVE
```


Dalga.

### WEAVE {#WEAVE}
```
public static int WEAVE
```


Dokuma.

### WIDE_DOWNWARD_DIAGONAL {#WIDE-DOWNWARD-DIAGONAL}
```
public static int WIDE_DOWNWARD_DIAGONAL
```


Geniş aşağı doğru diyagonal.

### WIDE_UPWARD_DIAGONAL {#WIDE-UPWARD-DIAGONAL}
```
public static int WIDE_UPWARD_DIAGONAL
```


Geniş yukarı doğru diyagonal.

### ZIG_ZAG {#ZIG-ZAG}
```
public static int ZIG_ZAG
```


Zikzak.

### length {#length}
```
public static int length
```


### fromName(String patternTypeName) {#fromName-java.lang.String}
```
public static int fromName(String patternTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| patternTypeName | java.lang.String |  |

**Returns:**
int
### getName(int patternType) {#getName-int}
```
public static String getName(int patternType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| patternType | int |  |

**Returns:**
java.lang.String
