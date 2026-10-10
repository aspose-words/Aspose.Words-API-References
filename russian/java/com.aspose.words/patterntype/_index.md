---
title: "PatternType"
linktitle: "PatternType"
second_title: "Aspose.Words для Java"
description: "Указывает шаблон заливки, который будет использоваться для заполнения фигуры в Java."
type: docs
weight: 526
url: /ru/java/com.aspose.words/patterntype/
---

**Inheritance:**
java.lang.Object
```
public class PatternType
```

Указывает шаблон заливки, используемый для заполнения фигуры.

 **Examples:** 

Показывает, как установить узор для фигуры.

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
## Поля

| Поле | Описание |
| --- | --- |
| [CROSS](#CROSS) | Крест. |
| [DARK_DOWNWARD_DIAGONAL](#DARK-DOWNWARD-DIAGONAL) | Темная нисходящая диагональ. |
| [DARK_HORIZONTAL](#DARK-HORIZONTAL) | Темная горизонтальная. |
| [DARK_UPWARD_DIAGONAL](#DARK-UPWARD-DIAGONAL) | Темная восходящая диагональ. |
| [DARK_VERTICAL](#DARK-VERTICAL) | Темная вертикальная. |
| [DASHED_DOWNWARD_DIAGONAL](#DASHED-DOWNWARD-DIAGONAL) | Пунктирная нисходящая диагональ. |
| [DASHED_HORIZONTAL](#DASHED-HORIZONTAL) | Пунктирная горизонтальная. |
| [DASHED_UPWARD_DIAGONAL](#DASHED-UPWARD-DIAGONAL) | Пунктирная восходящая диагональ. |
| [DASHED_VERTICAL](#DASHED-VERTICAL) | Пунктирная вертикальная. |
| [DIAGONAL_BRICK](#DIAGONAL-BRICK) | Диагональная кирпичная. |
| [DIAGONAL_CROSS](#DIAGONAL-CROSS) | Диагональный крест. |
| [DIVOT](#DIVOT) | Вмятина шаблона. |
| [DOTTED_DIAMOND](#DOTTED-DIAMOND) | Точечный ромб. |
| [DOTTED_GRID](#DOTTED-GRID) | Точечная сетка. |
| [DOWNWARD_DIAGONAL](#DOWNWARD-DIAGONAL) | Нисходящая диагональ. |
| [HORIZONTAL](#HORIZONTAL) | Горизонтальная. |
| [HORIZONTAL_BRICK](#HORIZONTAL-BRICK) | Горизонтальная кирпичная. |
| [LARGE_CHECKER_BOARD](#LARGE-CHECKER-BOARD) | Большая шахматная доска. |
| [LARGE_CONFETTI](#LARGE-CONFETTI) | Большой конфетти. |
| [LARGE_GRID](#LARGE-GRID) | Большая сетка. |
| [LIGHT_DOWNWARD_DIAGONAL](#LIGHT-DOWNWARD-DIAGONAL) | Светлая диагональ вниз. |
| [LIGHT_HORIZONTAL](#LIGHT-HORIZONTAL) | Светлая горизонтальная. |
| [LIGHT_UPWARD_DIAGONAL](#LIGHT-UPWARD-DIAGONAL) | Светлая диагональ вверх. |
| [LIGHT_VERTICAL](#LIGHT-VERTICAL) | Светлая вертикальная. |
| [NARROW_HORIZONTAL](#NARROW-HORIZONTAL) | Узкая горизонтальная. |
| [NARROW_VERTICAL](#NARROW-VERTICAL) | Узкая вертикальная. |
| [NONE](#NONE) | Без узора. |
| [OUTLINED_DIAMOND](#OUTLINED-DIAMOND) | Контурный ромб. |
| [PERCENT_10](#PERCENT-10) | 10% цвета переднего плана. |
| [PERCENT_20](#PERCENT-20) | 20% цвета переднего плана. |
| [PERCENT_25](#PERCENT-25) | 25% цвета переднего плана. |
| [PERCENT_30](#PERCENT-30) | 30% цвета переднего плана. |
| [PERCENT_40](#PERCENT-40) | 40% цвета переднего плана |
| [PERCENT_5](#PERCENT-5) | 5% цвета переднего плана. |
| [PERCENT_50](#PERCENT-50) | 50% цвета переднего плана |
| [PERCENT_60](#PERCENT-60) | 60% цвета переднего плана. |
| [PERCENT_70](#PERCENT-70) | 70% цвета переднего плана. |
| [PERCENT_75](#PERCENT-75) | 75% цвета переднего плана. |
| [PERCENT_80](#PERCENT-80) | 80% цвета переднего плана. |
| [PERCENT_90](#PERCENT-90) | 90% цвета переднего плана. |
| [PLAID](#PLAID) | Клетка. |
| [SHINGLE](#SHINGLE) | Гонт. |
| [SMALL_CHECKER_BOARD](#SMALL-CHECKER-BOARD) | Небольшая шахматная доска. |
| [SMALL_CONFETTI](#SMALL-CONFETTI) | Мелкие конфетти. |
| [SMALL_GRID](#SMALL-GRID) | Маленькая сетка. |
| [SOLID_DIAMOND](#SOLID-DIAMOND) | Сплошной ромб. |
| [SPHERE](#SPHERE) | Сфера. |
| [TRELLIS](#TRELLIS) | Решетка. |
| [UPWARD_DIAGONAL](#UPWARD-DIAGONAL) | Диагональ вверх. |
| [VERTICAL](#VERTICAL) | Вертикальная. |
| [WAVE](#WAVE) | Волна. |
| [WEAVE](#WEAVE) | Плетение. |
| [WIDE_DOWNWARD_DIAGONAL](#WIDE-DOWNWARD-DIAGONAL) | Широкая диагональ вниз. |
| [WIDE_UPWARD_DIAGONAL](#WIDE-UPWARD-DIAGONAL) | Широкая диагональ вверх. |
| [ZIG_ZAG](#ZIG-ZAG) | Зигзаг. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String patternTypeName)](#fromName-java.lang.String) |  |
| [getName(int patternType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int patternType)](#toString-int) |  |
### CROSS {#CROSS}
```
public static int CROSS
```


Крест.

### DARK_DOWNWARD_DIAGONAL {#DARK-DOWNWARD-DIAGONAL}
```
public static int DARK_DOWNWARD_DIAGONAL
```


Темная нисходящая диагональ.

### DARK_HORIZONTAL {#DARK-HORIZONTAL}
```
public static int DARK_HORIZONTAL
```


Темная горизонтальная.

### DARK_UPWARD_DIAGONAL {#DARK-UPWARD-DIAGONAL}
```
public static int DARK_UPWARD_DIAGONAL
```


Темная восходящая диагональ.

### DARK_VERTICAL {#DARK-VERTICAL}
```
public static int DARK_VERTICAL
```


Темная вертикальная.

### DASHED_DOWNWARD_DIAGONAL {#DASHED-DOWNWARD-DIAGONAL}
```
public static int DASHED_DOWNWARD_DIAGONAL
```


Пунктирная нисходящая диагональ.

### DASHED_HORIZONTAL {#DASHED-HORIZONTAL}
```
public static int DASHED_HORIZONTAL
```


Пунктирная горизонтальная.

### DASHED_UPWARD_DIAGONAL {#DASHED-UPWARD-DIAGONAL}
```
public static int DASHED_UPWARD_DIAGONAL
```


Пунктирная восходящая диагональ.

### DASHED_VERTICAL {#DASHED-VERTICAL}
```
public static int DASHED_VERTICAL
```


Пунктирная вертикальная.

### DIAGONAL_BRICK {#DIAGONAL-BRICK}
```
public static int DIAGONAL_BRICK
```


Диагональная кирпичная.

### DIAGONAL_CROSS {#DIAGONAL-CROSS}
```
public static int DIAGONAL_CROSS
```


Диагональный крест.

### DIVOT {#DIVOT}
```
public static int DIVOT
```


Вмятина шаблона.

### DOTTED_DIAMOND {#DOTTED-DIAMOND}
```
public static int DOTTED_DIAMOND
```


Точечный ромб.

### DOTTED_GRID {#DOTTED-GRID}
```
public static int DOTTED_GRID
```


Точечная сетка.

### DOWNWARD_DIAGONAL {#DOWNWARD-DIAGONAL}
```
public static int DOWNWARD_DIAGONAL
```


Нисходящая диагональ.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Горизонтальная.

### HORIZONTAL_BRICK {#HORIZONTAL-BRICK}
```
public static int HORIZONTAL_BRICK
```


Горизонтальная кирпичная.

### LARGE_CHECKER_BOARD {#LARGE-CHECKER-BOARD}
```
public static int LARGE_CHECKER_BOARD
```


Большая шахматная доска.

### LARGE_CONFETTI {#LARGE-CONFETTI}
```
public static int LARGE_CONFETTI
```


Большой конфетти.

### LARGE_GRID {#LARGE-GRID}
```
public static int LARGE_GRID
```


Большая сетка.

### LIGHT_DOWNWARD_DIAGONAL {#LIGHT-DOWNWARD-DIAGONAL}
```
public static int LIGHT_DOWNWARD_DIAGONAL
```


Светлая диагональ вниз.

### LIGHT_HORIZONTAL {#LIGHT-HORIZONTAL}
```
public static int LIGHT_HORIZONTAL
```


Светлая горизонтальная.

### LIGHT_UPWARD_DIAGONAL {#LIGHT-UPWARD-DIAGONAL}
```
public static int LIGHT_UPWARD_DIAGONAL
```


Светлая диагональ вверх.

### LIGHT_VERTICAL {#LIGHT-VERTICAL}
```
public static int LIGHT_VERTICAL
```


Светлая вертикальная.

### NARROW_HORIZONTAL {#NARROW-HORIZONTAL}
```
public static int NARROW_HORIZONTAL
```


Узкая горизонтальная.

### NARROW_VERTICAL {#NARROW-VERTICAL}
```
public static int NARROW_VERTICAL
```


Узкая вертикальная.

### NONE {#NONE}
```
public static int NONE
```


Без узора.

### OUTLINED_DIAMOND {#OUTLINED-DIAMOND}
```
public static int OUTLINED_DIAMOND
```


Контурный ромб.

### PERCENT_10 {#PERCENT-10}
```
public static int PERCENT_10
```


10% цвета переднего плана.

### PERCENT_20 {#PERCENT-20}
```
public static int PERCENT_20
```


20% цвета переднего плана.

### PERCENT_25 {#PERCENT-25}
```
public static int PERCENT_25
```


25% цвета переднего плана.

### PERCENT_30 {#PERCENT-30}
```
public static int PERCENT_30
```


30% цвета переднего плана.

### PERCENT_40 {#PERCENT-40}
```
public static int PERCENT_40
```


40% цвета переднего плана

### PERCENT_5 {#PERCENT-5}
```
public static int PERCENT_5
```


5% цвета переднего плана.

### PERCENT_50 {#PERCENT-50}
```
public static int PERCENT_50
```


50% цвета переднего плана

### PERCENT_60 {#PERCENT-60}
```
public static int PERCENT_60
```


60% цвета переднего плана.

### PERCENT_70 {#PERCENT-70}
```
public static int PERCENT_70
```


70% цвета переднего плана.

### PERCENT_75 {#PERCENT-75}
```
public static int PERCENT_75
```


75% цвета переднего плана.

### PERCENT_80 {#PERCENT-80}
```
public static int PERCENT_80
```


80% цвета переднего плана.

### PERCENT_90 {#PERCENT-90}
```
public static int PERCENT_90
```


90% цвета переднего плана.

### PLAID {#PLAID}
```
public static int PLAID
```


Клетка.

### SHINGLE {#SHINGLE}
```
public static int SHINGLE
```


Гонт.

### SMALL_CHECKER_BOARD {#SMALL-CHECKER-BOARD}
```
public static int SMALL_CHECKER_BOARD
```


Небольшая шахматная доска.

### SMALL_CONFETTI {#SMALL-CONFETTI}
```
public static int SMALL_CONFETTI
```


Мелкие конфетти.

### SMALL_GRID {#SMALL-GRID}
```
public static int SMALL_GRID
```


Маленькая сетка.

### SOLID_DIAMOND {#SOLID-DIAMOND}
```
public static int SOLID_DIAMOND
```


Сплошной ромб.

### SPHERE {#SPHERE}
```
public static int SPHERE
```


Сфера.

### TRELLIS {#TRELLIS}
```
public static int TRELLIS
```


Решетка.

### UPWARD_DIAGONAL {#UPWARD-DIAGONAL}
```
public static int UPWARD_DIAGONAL
```


Диагональ вверх.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Вертикальная.

### WAVE {#WAVE}
```
public static int WAVE
```


Волна.

### WEAVE {#WEAVE}
```
public static int WEAVE
```


Плетение.

### WIDE_DOWNWARD_DIAGONAL {#WIDE-DOWNWARD-DIAGONAL}
```
public static int WIDE_DOWNWARD_DIAGONAL
```


Широкая диагональ вниз.

### WIDE_UPWARD_DIAGONAL {#WIDE-UPWARD-DIAGONAL}
```
public static int WIDE_UPWARD_DIAGONAL
```


Широкая диагональ вверх.

### ZIG_ZAG {#ZIG-ZAG}
```
public static int ZIG_ZAG
```


Зигзаг.

### length {#length}
```
public static int length
```


### fromName(String patternTypeName) {#fromName-java.lang.String}
```
public static int fromName(String patternTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| patternTypeName | java.lang.String |  |

**Returns:**
int
### getName(int patternType) {#getName-int}
```
public static String getName(int patternType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| patternType | int |  |

**Returns:**
java.lang.String
