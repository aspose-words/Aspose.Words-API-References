---
title: "ShapeTextOrientation"
linktitle: "ShapeTextOrientation"
second_title: "Aspose.Words for Java"
description: "指定在 Java 中形状中文本的方向。"
type: docs
weight: 617
url: /zh/java/com.aspose.words/shapetextorientation/
---

**Inheritance:**
java.lang.Object
```
public class ShapeTextOrientation
```

指定形状中文本的方向。

 **Examples:** 

展示如何更改数据标签的方向和旋转。

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
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [DOWNWARD](#DOWNWARD) | 文本向右旋转 90 度，以实现从上到下显示 (tb-rl)。 |
| [HORIZONTAL](#HORIZONTAL) | 文本水平排列 (lr-tb)。 |
| [UPWARD](#UPWARD) | 文本向左旋转 90 度，以实现从下到上显示 (bt-lr)。 |
| [VERTICAL_FAR_EAST](#VERTICAL-FAR-EAST) | 东亚字符垂直显示，其他文本向右旋转 90 度，以实现从上到下显示 (tb-rl-v)。 |
| [VERTICAL_ROTATED_FAR_EAST](#VERTICAL-ROTATED-FAR-EAST) | 东亚字符呈垂直显示，其他文本向右旋转 90 度，以从上到下垂直显示，然后从左到右水平显示 (tb-lr-v)。 |
| [WORD_ART_VERTICAL](#WORD-ART-VERTICAL) | 文本垂直排列，字母上下堆叠。 |
| [WORD_ART_VERTICAL_RIGHT_TO_LEFT](#WORD-ART-VERTICAL-RIGHT-TO-LEFT) | 文本垂直排列，字母上下堆叠，然后水平从右到左。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String shapeTextOrientationName)](#fromName-java.lang.String) |  |
| [getName(int shapeTextOrientation)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeTextOrientation)](#toString-int) |  |
### DOWNWARD {#DOWNWARD}
```
public static int DOWNWARD
```


文本向右旋转 90 度，以实现从上到下显示 (tb-rl)。

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


文本水平排列 (lr-tb)。

### UPWARD {#UPWARD}
```
public static int UPWARD
```


文本向左旋转 90 度，以实现从下到上显示 (bt-lr)。

### VERTICAL_FAR_EAST {#VERTICAL-FAR-EAST}
```
public static int VERTICAL_FAR_EAST
```


东亚字符垂直显示，其他文本向右旋转 90 度，以实现从上到下显示 (tb-rl-v)。

### VERTICAL_ROTATED_FAR_EAST {#VERTICAL-ROTATED-FAR-EAST}
```
public static int VERTICAL_ROTATED_FAR_EAST
```


东亚字符呈垂直显示，其他文本向右旋转 90 度，以从上到下垂直显示，然后从左到右水平显示 (tb-lr-v)。

### WORD_ART_VERTICAL {#WORD-ART-VERTICAL}
```
public static int WORD_ART_VERTICAL
```


文本垂直排列，字母上下堆叠。

### WORD_ART_VERTICAL_RIGHT_TO_LEFT {#WORD-ART-VERTICAL-RIGHT-TO-LEFT}
```
public static int WORD_ART_VERTICAL_RIGHT_TO_LEFT
```


文本垂直排列，字母上下堆叠，然后水平从右到左。

### length {#length}
```
public static int length
```


### fromName(String shapeTextOrientationName) {#fromName-java.lang.String}
```
public static int fromName(String shapeTextOrientationName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| shapeTextOrientationName | java.lang.String |  |

**Returns:**
int
### getName(int shapeTextOrientation) {#getName-int}
```
public static String getName(int shapeTextOrientation)
```




**Parameters:**
| 参数 | 类型 | 描述 |
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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| shapeTextOrientation | int |  |

**Returns:**
java.lang.String
