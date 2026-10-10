---
title: "ChartDataLabelPosition"
linktitle: "ChartDataLabelPosition"
second_title: "Aspose.Words Java için"
description: "Java'da bir grafik veri etiketinin konumunu belirtir."
type: docs
weight: 74
url: /tr/java/com.aspose.words/chartdatalabelposition/
---

**Inheritance:**
java.lang.Object
```
public class ChartDataLabelPosition
```

Grafik veri etiketi için konumu belirtir.

 **Remarks:** 

Tüm seri tipleri etiket konumlarını belirtmenize izin vermez. İzin verenler bile tüm değerleri desteklemez.

 **Examples:** 

Veri etiketinin konumunun nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert column chart.
 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();

 // Delete default generated series.
 seriesColl.clear();

 // Add series.
 ChartSeries series = seriesColl.add(
         "Series 1",
         new String[] { "Category 1", "Category 2", "Category 3" },
         new double[] { 4.0, 5.0, 6.0 });

 // Show data labels and set font color.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.getFont().setColor(Color.WHITE);

 // Set data label position.
 dataLabels.setPosition(ChartDataLabelPosition.INSIDE_BASE);
 dataLabels.get(0).setPosition(ChartDataLabelPosition.OUTSIDE_END);
 dataLabels.get(0).getFont().setColor(Color.RED);

 doc.save(getArtifactsDir() + "Charts.LabelPosition.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ABOVE](#ABOVE) | Bir veri etiketinin veri işaretçisinin üzerinde görüntülenmesi gerektiğini belirtir. |
| [BELOW](#BELOW) | Bir veri etiketinin veri işaretçisinin altında görüntülenmesi gerektiğini belirtir. |
| [BEST_FIT](#BEST-FIT) | Bir veri etiketinin en uygun konumda görüntülenmesi gerektiğini belirtir. |
| [CENTER](#CENTER) | Bir veri etiketinin veri işaretçisinin ortasında görüntülenmesi gerektiğini belirtir. |
| [INSIDE_BASE](#INSIDE-BASE) | Bir veri etiketinin veri işaretçisinin tabanının içinde görüntülenmesi gerektiğini belirtir. |
| [INSIDE_END](#INSIDE-END) | Bir veri etiketinin veri işaretçisinin ucunun içinde görüntülenmesi gerektiğini belirtir. |
| [LEFT](#LEFT) | Bir veri etiketinin veri işaretçisinin solunda görüntülenmesi gerektiğini belirtir. |
| [OUTSIDE_END](#OUTSIDE-END) | Bir veri etiketinin veri işaretçisinin ucunun dışında görüntülenmesi gerektiğini belirtir. |
| [RIGHT](#RIGHT) | Bir veri etiketinin veri işaretçisinin sağında görüntülenmesi gerektiğini belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String chartDataLabelPositionName)](#fromName-java.lang.String) |  |
| [getName(int chartDataLabelPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartDataLabelPosition)](#toString-int) |  |
### ABOVE {#ABOVE}
```
public static int ABOVE
```


Bir veri etiketinin veri işaretçisinin üzerinde görüntülenmesi gerektiğini belirtir.

### BELOW {#BELOW}
```
public static int BELOW
```


Bir veri etiketinin veri işaretçisinin altında görüntülenmesi gerektiğini belirtir.

### BEST_FIT {#BEST-FIT}
```
public static int BEST_FIT
```


Bir veri etiketinin en uygun konumda görüntülenmesi gerektiğini belirtir.

### CENTER {#CENTER}
```
public static int CENTER
```


Bir veri etiketinin veri işaretçisinin ortasında görüntülenmesi gerektiğini belirtir.

### INSIDE_BASE {#INSIDE-BASE}
```
public static int INSIDE_BASE
```


Bir veri etiketinin veri işaretçisinin tabanının içinde görüntülenmesi gerektiğini belirtir.

### INSIDE_END {#INSIDE-END}
```
public static int INSIDE_END
```


Bir veri etiketinin veri işaretçisinin ucunun içinde görüntülenmesi gerektiğini belirtir.

### LEFT {#LEFT}
```
public static int LEFT
```


Bir veri etiketinin veri işaretçisinin solunda görüntülenmesi gerektiğini belirtir.

### OUTSIDE_END {#OUTSIDE-END}
```
public static int OUTSIDE_END
```


Bir veri etiketinin veri işaretçisinin ucunun dışında görüntülenmesi gerektiğini belirtir.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Bir veri etiketinin veri işaretçisinin sağında görüntülenmesi gerektiğini belirtir.

### length {#length}
```
public static int length
```


### fromName(String chartDataLabelPositionName) {#fromName-java.lang.String}
```
public static int fromName(String chartDataLabelPositionName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartDataLabelPositionName | java.lang.String |  |

**Returns:**
int
### getName(int chartDataLabelPosition) {#getName-int}
```
public static String getName(int chartDataLabelPosition)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartDataLabelPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chartDataLabelPosition) {#toString-int}
```
public static String toString(int chartDataLabelPosition)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartDataLabelPosition | int |  |

**Returns:**
java.lang.String
