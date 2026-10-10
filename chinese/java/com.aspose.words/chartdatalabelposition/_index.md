---
title: "ChartDataLabelPosition"
linktitle: "ChartDataLabelPosition"
second_title: "Aspose.Words for Java"
description: "指定 Java 中图表数据标签的位置。"
type: docs
weight: 74
url: /zh/java/com.aspose.words/chartdatalabelposition/
---

**Inheritance:**
java.lang.Object
```
public class ChartDataLabelPosition
```

指定图表数据标签的位置。

 **Remarks:** 

并非所有系列类型都允许指定标签位置。而能够的，也不支持所有值。

 **Examples:** 

展示如何设置数据标签的位置。

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
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [ABOVE](#ABOVE) | 指定数据标签应显示在数据标记的上方。 |
| [BELOW](#BELOW) | 指定数据标签应显示在数据标记的下方。 |
| [BEST_FIT](#BEST-FIT) | 指定数据标签应显示在最合适的位置。 |
| [CENTER](#CENTER) | 指定应在数据标记上居中显示数据标签。 |
| [INSIDE_BASE](#INSIDE-BASE) | 指定应在数据标记的基部内部显示数据标签。 |
| [INSIDE_END](#INSIDE-END) | 指定应在数据标记的末端内部显示数据标签。 |
| [LEFT](#LEFT) | 指定应在数据标记左侧显示数据标签。 |
| [OUTSIDE_END](#OUTSIDE-END) | 指定应在数据标记的末端外部显示数据标签。 |
| [RIGHT](#RIGHT) | 指定应在数据标记右侧显示数据标签。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String chartDataLabelPositionName)](#fromName-java.lang.String) |  |
| [getName(int chartDataLabelPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartDataLabelPosition)](#toString-int) |  |
### ABOVE {#ABOVE}
```
public static int ABOVE
```


指定数据标签应显示在数据标记的上方。

### BELOW {#BELOW}
```
public static int BELOW
```


指定数据标签应显示在数据标记的下方。

### BEST_FIT {#BEST-FIT}
```
public static int BEST_FIT
```


指定数据标签应显示在最合适的位置。

### CENTER {#CENTER}
```
public static int CENTER
```


指定应在数据标记上居中显示数据标签。

### INSIDE_BASE {#INSIDE-BASE}
```
public static int INSIDE_BASE
```


指定应在数据标记的基部内部显示数据标签。

### INSIDE_END {#INSIDE-END}
```
public static int INSIDE_END
```


指定应在数据标记的末端内部显示数据标签。

### LEFT {#LEFT}
```
public static int LEFT
```


指定应在数据标记左侧显示数据标签。

### OUTSIDE_END {#OUTSIDE-END}
```
public static int OUTSIDE_END
```


指定应在数据标记的末端外部显示数据标签。

### RIGHT {#RIGHT}
```
public static int RIGHT
```


指定应在数据标记右侧显示数据标签。

### length {#length}
```
public static int length
```


### fromName(String chartDataLabelPositionName) {#fromName-java.lang.String}
```
public static int fromName(String chartDataLabelPositionName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| chartDataLabelPositionName | java.lang.String |  |

**Returns:**
int
### getName(int chartDataLabelPosition) {#getName-int}
```
public static String getName(int chartDataLabelPosition)
```




**Parameters:**
| 参数 | 类型 | 描述 |
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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| chartDataLabelPosition | int |  |

**Returns:**
java.lang.String
