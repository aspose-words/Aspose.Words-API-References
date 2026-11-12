---
title: "ShapeTextOrientation"
linktitle: "ShapeTextOrientation"
second_title: "Aspose.Words для Java"
description: "Указывает ориентацию текста в фигурах в Java."
type: docs
weight: 617
url: /ru/java/com.aspose.words/shapetextorientation/
---

**Inheritance:**
java.lang.Object
```
public class ShapeTextOrientation
```

Указывает ориентацию текста в фигурах.

 **Examples:** 

Показывает, как изменить ориентацию и вращение меток данных.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 ChartSeries series = shape.getChart().getSeries().get(0);
 ChartDataLabelCollection dataLabels = series.getDataLabels();

 // Show data labels.
 series.hasDataLabels(true);
 dataLabels.setShowValue(true);
 dataLabels.setShowCategoryName(true);

 // Define data label shape.
 dataLabels.getFormat().setShapeType(ChartShapeType.UP_ARROW);
 dataLabels.getFormat().getStroke().getFill().solid(Color.blue);

 // Set data label orientation and rotation for the entire series.
 dataLabels.setOrientation(ShapeTextOrientation.VERTICAL_FAR_EAST);
 dataLabels.setRotation(-45);

 // Change orientation and rotation of the first data label.
 dataLabels.get(0).setOrientation(ShapeTextOrientation.HORIZONTAL);
 dataLabels.get(0).setRotation(45);

 doc.save(getArtifactsDir() + "Charts.LabelOrientationRotation.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [DOWNWARD](#DOWNWARD) | Текст вращается на 90 градусов вправо, чтобы отображаться сверху вниз (tb-rl). |
| [HORIZONTAL](#HORIZONTAL) | Текст располагается горизонтально (lr-tb). |
| [UPWARD](#UPWARD) | Текст вращается на 90 градусов влево, чтобы отображаться снизу вверх (bt-lr). |
| [VERTICAL_FAR_EAST](#VERTICAL-FAR-EAST) | Символы Дальнего Востока отображаются вертикально, остальной текст вращается на 90 градусов вправо, чтобы отображаться сверху вниз (tb-rl-v). |
| [VERTICAL_ROTATED_FAR_EAST](#VERTICAL-ROTATED-FAR-EAST) | Символы Дальнего Востока отображаются вертикально, другой текст повернут на 90 градусов вправо, чтобы отображаться сверху вниз вертикально, затем слева направо горизонтально (tb-lr-v). |
| [WORD_ART_VERTICAL](#WORD-ART-VERTICAL) | Текст расположен вертикально, по одной букве друг над другом. |
| [WORD_ART_VERTICAL_RIGHT_TO_LEFT](#WORD-ART-VERTICAL-RIGHT-TO-LEFT) | Текст расположен вертикально, по одной букве друг над другом, затем горизонтально справа налево. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String shapeTextOrientationName)](#fromName-java.lang.String) |  |
| [getName(int shapeTextOrientation)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeTextOrientation)](#toString-int) |  |
### DOWNWARD {#DOWNWARD}
```
public static int DOWNWARD
```


Текст вращается на 90 градусов вправо, чтобы отображаться сверху вниз (tb-rl).

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Текст располагается горизонтально (lr-tb).

### UPWARD {#UPWARD}
```
public static int UPWARD
```


Текст вращается на 90 градусов влево, чтобы отображаться снизу вверх (bt-lr).

### VERTICAL_FAR_EAST {#VERTICAL-FAR-EAST}
```
public static int VERTICAL_FAR_EAST
```


Символы Дальнего Востока отображаются вертикально, остальной текст вращается на 90 градусов вправо, чтобы отображаться сверху вниз (tb-rl-v).

### VERTICAL_ROTATED_FAR_EAST {#VERTICAL-ROTATED-FAR-EAST}
```
public static int VERTICAL_ROTATED_FAR_EAST
```


Символы Дальнего Востока отображаются вертикально, другой текст повернут на 90 градусов вправо, чтобы отображаться сверху вниз вертикально, затем слева направо горизонтально (tb-lr-v).

### WORD_ART_VERTICAL {#WORD-ART-VERTICAL}
```
public static int WORD_ART_VERTICAL
```


Текст расположен вертикально, по одной букве друг над другом.

### WORD_ART_VERTICAL_RIGHT_TO_LEFT {#WORD-ART-VERTICAL-RIGHT-TO-LEFT}
```
public static int WORD_ART_VERTICAL_RIGHT_TO_LEFT
```


Текст расположен вертикально, по одной букве друг над другом, затем горизонтально справа налево.

### length {#length}
```
public static int length
```


### fromName(String shapeTextOrientationName) {#fromName-java.lang.String}
```
public static int fromName(String shapeTextOrientationName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| shapeTextOrientationName | java.lang.String |  |

**Returns:**
int
### getName(int shapeTextOrientation) {#getName-int}
```
public static String getName(int shapeTextOrientation)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| shapeTextOrientation | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int shapeTextOrientation) {#toString-int}
```
public static String toString(int shapeTextOrientation)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| shapeTextOrientation | int |  |

**Returns:**
java.lang.String
