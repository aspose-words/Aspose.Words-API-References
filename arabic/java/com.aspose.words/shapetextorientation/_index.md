---
title: "ShapeTextOrientation"
linktitle: "ShapeTextOrientation"
second_title: "Aspose.Words لـ Java"
description: "يحدد اتجاه النص داخل الأشكال في Java."
type: docs
weight: 617
url: /ar/java/com.aspose.words/shapetextorientation/
---

**Inheritance:**
java.lang.Object
```
public class ShapeTextOrientation
```

يحدد اتجاه النص في الأشكال.

 **Examples:** 

يوضح كيفية تغيير الاتجاه والدوران لتسميات البيانات.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [DOWNWARD](#DOWNWARD) | النص مُدوَّر 90 درجة إلى اليمين ليظهر من الأعلى إلى الأسفل (tb-rl). |
| [HORIZONTAL](#HORIZONTAL) | النص مُرتب أفقيًا (lr-tb). |
| [UPWARD](#UPWARD) | النص مُدوَّر 90 درجة إلى اليسار ليظهر من الأسفل إلى الأعلى (bt-lr). |
| [VERTICAL_FAR_EAST](#VERTICAL-FAR-EAST) | أحرف الشرق الأقصى تظهر عموديًا، والنص الآخر مُدوَّر 90 درجة إلى اليمين ليظهر من الأعلى إلى الأسفل (tb-rl-v). |
| [VERTICAL_ROTATED_FAR_EAST](#VERTICAL-ROTATED-FAR-EAST) | تظهر أحرف الشرق الأقصى عمودية، والنص الآخر يتم تدويره 90 درجة إلى اليمين ليظهر من أعلى إلى أسفل عموديًا، ثم من اليسار إلى اليمين أفقيًا (tb-lr-v). |
| [WORD_ART_VERTICAL](#WORD-ART-VERTICAL) | النص عمودي، بحرف واحد فوق الآخر. |
| [WORD_ART_VERTICAL_RIGHT_TO_LEFT](#WORD-ART-VERTICAL-RIGHT-TO-LEFT) | النص عمودي، بحرف واحد فوق الآخر، ثم من اليمين إلى اليسار أفقيًا. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String shapeTextOrientationName)](#fromName-java.lang.String) |  |
| [getName(int shapeTextOrientation)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeTextOrientation)](#toString-int) |  |
### DOWNWARD {#DOWNWARD}
```
public static int DOWNWARD
```


النص مُدوَّر 90 درجة إلى اليمين ليظهر من الأعلى إلى الأسفل (tb-rl).

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


النص مُرتب أفقيًا (lr-tb).

### UPWARD {#UPWARD}
```
public static int UPWARD
```


النص مُدوَّر 90 درجة إلى اليسار ليظهر من الأسفل إلى الأعلى (bt-lr).

### VERTICAL_FAR_EAST {#VERTICAL-FAR-EAST}
```
public static int VERTICAL_FAR_EAST
```


أحرف الشرق الأقصى تظهر عموديًا، والنص الآخر مُدوَّر 90 درجة إلى اليمين ليظهر من الأعلى إلى الأسفل (tb-rl-v).

### VERTICAL_ROTATED_FAR_EAST {#VERTICAL-ROTATED-FAR-EAST}
```
public static int VERTICAL_ROTATED_FAR_EAST
```


تظهر أحرف الشرق الأقصى عمودية، والنص الآخر يتم تدويره 90 درجة إلى اليمين ليظهر من أعلى إلى أسفل عموديًا، ثم من اليسار إلى اليمين أفقيًا (tb-lr-v).

### WORD_ART_VERTICAL {#WORD-ART-VERTICAL}
```
public static int WORD_ART_VERTICAL
```


النص عمودي، بحرف واحد فوق الآخر.

### WORD_ART_VERTICAL_RIGHT_TO_LEFT {#WORD-ART-VERTICAL-RIGHT-TO-LEFT}
```
public static int WORD_ART_VERTICAL_RIGHT_TO_LEFT
```


النص عمودي، بحرف واحد فوق الآخر، ثم من اليمين إلى اليسار أفقيًا.

### length {#length}
```
public static int length
```


### fromName(String shapeTextOrientationName) {#fromName-java.lang.String}
```
public static int fromName(String shapeTextOrientationName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| shapeTextOrientationName | java.lang.String |  |

**Returns:**
int
### getName(int shapeTextOrientation) {#getName-int}
```
public static String getName(int shapeTextOrientation)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| shapeTextOrientation | int |  |

**Returns:**
java.lang.String
