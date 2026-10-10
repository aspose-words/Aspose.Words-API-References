---
title: "PatternType"
linktitle: "PatternType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نمط التعبئة الذي سيُستخدم لملء شكل في Java."
type: docs
weight: 526
url: /ar/java/com.aspose.words/patterntype/
---

**Inheritance:**
java.lang.Object
```
public class PatternType
```

يحدد نمط التعبئة الذي سيُستخدم لملء الشكل.

 **Examples:** 

يعرض كيفية تعيين نمط لشكل.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [CROSS](#CROSS) | صليب. |
| [DARK_DOWNWARD_DIAGONAL](#DARK-DOWNWARD-DIAGONAL) | قطرية سفلية داكنة. |
| [DARK_HORIZONTAL](#DARK-HORIZONTAL) | أفقي داكن. |
| [DARK_UPWARD_DIAGONAL](#DARK-UPWARD-DIAGONAL) | قطرية علوية داكنة. |
| [DARK_VERTICAL](#DARK-VERTICAL) | عمودي داكن. |
| [DASHED_DOWNWARD_DIAGONAL](#DASHED-DOWNWARD-DIAGONAL) | قطرية سفلية متقطعة. |
| [DASHED_HORIZONTAL](#DASHED-HORIZONTAL) | أفقي متقطعة. |
| [DASHED_UPWARD_DIAGONAL](#DASHED-UPWARD-DIAGONAL) | قطرية علوية متقطعة. |
| [DASHED_VERTICAL](#DASHED-VERTICAL) | عمودي متقطع. |
| [DIAGONAL_BRICK](#DIAGONAL-BRICK) | قالب طوب مائل. |
| [DIAGONAL_CROSS](#DIAGONAL-CROSS) | صليب مائل. |
| [DIVOT](#DIVOT) | نقطة نمط. |
| [DOTTED_DIAMOND](#DOTTED-DIAMOND) | ماسة منقطة. |
| [DOTTED_GRID](#DOTTED-GRID) | شبكة منقطة. |
| [DOWNWARD_DIAGONAL](#DOWNWARD-DIAGONAL) | قطرية سفلية. |
| [HORIZONTAL](#HORIZONTAL) | أفقي. |
| [HORIZONTAL_BRICK](#HORIZONTAL-BRICK) | قالب طوب أفقي. |
| [LARGE_CHECKER_BOARD](#LARGE-CHECKER-BOARD) | لوح شطرنج كبير. |
| [LARGE_CONFETTI](#LARGE-CONFETTI) | قُرصات كبيرة. |
| [LARGE_GRID](#LARGE-GRID) | شبكة كبيرة. |
| [LIGHT_DOWNWARD_DIAGONAL](#LIGHT-DOWNWARD-DIAGONAL) | قطر مائل لأسفل خفيف. |
| [LIGHT_HORIZONTAL](#LIGHT-HORIZONTAL) | أفقي خفيف. |
| [LIGHT_UPWARD_DIAGONAL](#LIGHT-UPWARD-DIAGONAL) | قطر مائل لأعلى خفيف. |
| [LIGHT_VERTICAL](#LIGHT-VERTICAL) | عمودي خفيف. |
| [NARROW_HORIZONTAL](#NARROW-HORIZONTAL) | أفقي ضيق. |
| [NARROW_VERTICAL](#NARROW-VERTICAL) | عمودي ضيق. |
| [NONE](#NONE) | بدون نمط. |
| [OUTLINED_DIAMOND](#OUTLINED-DIAMOND) | معين محدد بالخط. |
| [PERCENT_10](#PERCENT-10) | 10٪ من لون المقدمة. |
| [PERCENT_20](#PERCENT-20) | 20٪ من لون المقدمة. |
| [PERCENT_25](#PERCENT-25) | 25٪ من لون المقدمة. |
| [PERCENT_30](#PERCENT-30) | 30٪ من لون المقدمة. |
| [PERCENT_40](#PERCENT-40) | 40٪ من لون المقدمة |
| [PERCENT_5](#PERCENT-5) | 5٪ من لون المقدمة. |
| [PERCENT_50](#PERCENT-50) | 50٪ من لون المقدمة |
| [PERCENT_60](#PERCENT-60) | 60٪ من لون المقدمة. |
| [PERCENT_70](#PERCENT-70) | 70٪ من لون المقدمة. |
| [PERCENT_75](#PERCENT-75) | 75٪ من لون المقدمة. |
| [PERCENT_80](#PERCENT-80) | 80٪ من لون المقدمة. |
| [PERCENT_90](#PERCENT-90) | 90٪ من لون المقدمة. |
| [PLAID](#PLAID) | نقشة مربّعة. |
| [SHINGLE](#SHINGLE) | قالب قرميدي. |
| [SMALL_CHECKER_BOARD](#SMALL-CHECKER-BOARD) | لوحة شطرنج صغيرة. |
| [SMALL_CONFETTI](#SMALL-CONFETTI) | قُرص صغير. |
| [SMALL_GRID](#SMALL-GRID) | شبكة صغيرة. |
| [SOLID_DIAMOND](#SOLID-DIAMOND) | ماسة صلبة. |
| [SPHERE](#SPHERE) | كرة. |
| [TRELLIS](#TRELLIS) | شبكة تعريش. |
| [UPWARD_DIAGONAL](#UPWARD-DIAGONAL) | قطر صاعد. |
| [VERTICAL](#VERTICAL) | عمودي. |
| [WAVE](#WAVE) | موجة. |
| [WEAVE](#WEAVE) | نقش. |
| [WIDE_DOWNWARD_DIAGONAL](#WIDE-DOWNWARD-DIAGONAL) | قطر سفلي واسع. |
| [WIDE_UPWARD_DIAGONAL](#WIDE-UPWARD-DIAGONAL) | قطر صاعد واسع. |
| [ZIG_ZAG](#ZIG-ZAG) | متعرج. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String patternTypeName)](#fromName-java.lang.String) |  |
| [getName(int patternType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int patternType)](#toString-int) |  |
### CROSS {#CROSS}
```
public static int CROSS
```


صليب.

### DARK_DOWNWARD_DIAGONAL {#DARK-DOWNWARD-DIAGONAL}
```
public static int DARK_DOWNWARD_DIAGONAL
```


قطرية سفلية داكنة.

### DARK_HORIZONTAL {#DARK-HORIZONTAL}
```
public static int DARK_HORIZONTAL
```


أفقي داكن.

### DARK_UPWARD_DIAGONAL {#DARK-UPWARD-DIAGONAL}
```
public static int DARK_UPWARD_DIAGONAL
```


قطرية علوية داكنة.

### DARK_VERTICAL {#DARK-VERTICAL}
```
public static int DARK_VERTICAL
```


عمودي داكن.

### DASHED_DOWNWARD_DIAGONAL {#DASHED-DOWNWARD-DIAGONAL}
```
public static int DASHED_DOWNWARD_DIAGONAL
```


قطرية سفلية متقطعة.

### DASHED_HORIZONTAL {#DASHED-HORIZONTAL}
```
public static int DASHED_HORIZONTAL
```


أفقي متقطعة.

### DASHED_UPWARD_DIAGONAL {#DASHED-UPWARD-DIAGONAL}
```
public static int DASHED_UPWARD_DIAGONAL
```


قطرية علوية متقطعة.

### DASHED_VERTICAL {#DASHED-VERTICAL}
```
public static int DASHED_VERTICAL
```


عمودي متقطع.

### DIAGONAL_BRICK {#DIAGONAL-BRICK}
```
public static int DIAGONAL_BRICK
```


قالب طوب مائل.

### DIAGONAL_CROSS {#DIAGONAL-CROSS}
```
public static int DIAGONAL_CROSS
```


صليب مائل.

### DIVOT {#DIVOT}
```
public static int DIVOT
```


نقطة نمط.

### DOTTED_DIAMOND {#DOTTED-DIAMOND}
```
public static int DOTTED_DIAMOND
```


ماسة منقطة.

### DOTTED_GRID {#DOTTED-GRID}
```
public static int DOTTED_GRID
```


شبكة منقطة.

### DOWNWARD_DIAGONAL {#DOWNWARD-DIAGONAL}
```
public static int DOWNWARD_DIAGONAL
```


قطرية سفلية.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


أفقي.

### HORIZONTAL_BRICK {#HORIZONTAL-BRICK}
```
public static int HORIZONTAL_BRICK
```


قالب طوب أفقي.

### LARGE_CHECKER_BOARD {#LARGE-CHECKER-BOARD}
```
public static int LARGE_CHECKER_BOARD
```


لوح شطرنج كبير.

### LARGE_CONFETTI {#LARGE-CONFETTI}
```
public static int LARGE_CONFETTI
```


قُرصات كبيرة.

### LARGE_GRID {#LARGE-GRID}
```
public static int LARGE_GRID
```


شبكة كبيرة.

### LIGHT_DOWNWARD_DIAGONAL {#LIGHT-DOWNWARD-DIAGONAL}
```
public static int LIGHT_DOWNWARD_DIAGONAL
```


قطر مائل لأسفل خفيف.

### LIGHT_HORIZONTAL {#LIGHT-HORIZONTAL}
```
public static int LIGHT_HORIZONTAL
```


أفقي خفيف.

### LIGHT_UPWARD_DIAGONAL {#LIGHT-UPWARD-DIAGONAL}
```
public static int LIGHT_UPWARD_DIAGONAL
```


قطر مائل لأعلى خفيف.

### LIGHT_VERTICAL {#LIGHT-VERTICAL}
```
public static int LIGHT_VERTICAL
```


عمودي خفيف.

### NARROW_HORIZONTAL {#NARROW-HORIZONTAL}
```
public static int NARROW_HORIZONTAL
```


أفقي ضيق.

### NARROW_VERTICAL {#NARROW-VERTICAL}
```
public static int NARROW_VERTICAL
```


عمودي ضيق.

### NONE {#NONE}
```
public static int NONE
```


بدون نمط.

### OUTLINED_DIAMOND {#OUTLINED-DIAMOND}
```
public static int OUTLINED_DIAMOND
```


معين محدد بالخط.

### PERCENT_10 {#PERCENT-10}
```
public static int PERCENT_10
```


10٪ من لون المقدمة.

### PERCENT_20 {#PERCENT-20}
```
public static int PERCENT_20
```


20٪ من لون المقدمة.

### PERCENT_25 {#PERCENT-25}
```
public static int PERCENT_25
```


25٪ من لون المقدمة.

### PERCENT_30 {#PERCENT-30}
```
public static int PERCENT_30
```


30٪ من لون المقدمة.

### PERCENT_40 {#PERCENT-40}
```
public static int PERCENT_40
```


40٪ من لون المقدمة

### PERCENT_5 {#PERCENT-5}
```
public static int PERCENT_5
```


5٪ من لون المقدمة.

### PERCENT_50 {#PERCENT-50}
```
public static int PERCENT_50
```


50٪ من لون المقدمة

### PERCENT_60 {#PERCENT-60}
```
public static int PERCENT_60
```


60٪ من لون المقدمة.

### PERCENT_70 {#PERCENT-70}
```
public static int PERCENT_70
```


70٪ من لون المقدمة.

### PERCENT_75 {#PERCENT-75}
```
public static int PERCENT_75
```


75٪ من لون المقدمة.

### PERCENT_80 {#PERCENT-80}
```
public static int PERCENT_80
```


80٪ من لون المقدمة.

### PERCENT_90 {#PERCENT-90}
```
public static int PERCENT_90
```


90٪ من لون المقدمة.

### PLAID {#PLAID}
```
public static int PLAID
```


نقشة مربّعة.

### SHINGLE {#SHINGLE}
```
public static int SHINGLE
```


قالب قرميدي.

### SMALL_CHECKER_BOARD {#SMALL-CHECKER-BOARD}
```
public static int SMALL_CHECKER_BOARD
```


لوحة شطرنج صغيرة.

### SMALL_CONFETTI {#SMALL-CONFETTI}
```
public static int SMALL_CONFETTI
```


قُرص صغير.

### SMALL_GRID {#SMALL-GRID}
```
public static int SMALL_GRID
```


شبكة صغيرة.

### SOLID_DIAMOND {#SOLID-DIAMOND}
```
public static int SOLID_DIAMOND
```


ماسة صلبة.

### SPHERE {#SPHERE}
```
public static int SPHERE
```


كرة.

### TRELLIS {#TRELLIS}
```
public static int TRELLIS
```


شبكة تعريش.

### UPWARD_DIAGONAL {#UPWARD-DIAGONAL}
```
public static int UPWARD_DIAGONAL
```


قطر صاعد.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


عمودي.

### WAVE {#WAVE}
```
public static int WAVE
```


موجة.

### WEAVE {#WEAVE}
```
public static int WEAVE
```


نقش.

### WIDE_DOWNWARD_DIAGONAL {#WIDE-DOWNWARD-DIAGONAL}
```
public static int WIDE_DOWNWARD_DIAGONAL
```


قطر سفلي واسع.

### WIDE_UPWARD_DIAGONAL {#WIDE-UPWARD-DIAGONAL}
```
public static int WIDE_UPWARD_DIAGONAL
```


قطر صاعد واسع.

### ZIG_ZAG {#ZIG-ZAG}
```
public static int ZIG_ZAG
```


متعرج.

### length {#length}
```
public static int length
```


### fromName(String patternTypeName) {#fromName-java.lang.String}
```
public static int fromName(String patternTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| patternTypeName | java.lang.String |  |

**Returns:**
int
### getName(int patternType) {#getName-int}
```
public static String getName(int patternType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| patternType | int |  |

**Returns:**
java.lang.String
