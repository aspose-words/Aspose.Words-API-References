---
title: "ChartXValueCollection"
linktitle: "ChartXValueCollection"
second_title: "Aspose.Words for Java"
description: "表示 Java 中图表系列的 X 值集合。"
type: docs
weight: 95
url: /zh/java/com.aspose.words/chartxvaluecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartXValueCollection implements Iterable
```

表示图表系列的 X 值集合。

 **Remarks:** 

集合中除 **null** 之外的所有项必须具有相同的 [ChartXValue.getValueType()](../../com.aspose.words/chartxvalue/\#getValueType)。

该集合仅允许更改 X 值。若要向图表系列添加或插入新值，或删除值，可使用 [ChartSeries](../../com.aspose.words/chartseries/) 类的相应方法。

 **Examples:** 

展示如何获取图表系列数据。

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder();

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series = chart.getSeries().get(0);

 double minValue = Double.MAX_VALUE;
 int minValueIndex = 0;
 double maxValue = -Double.MAX_VALUE;
 int maxValueIndex = 0;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     // Clear individual format of all data points.
     // Data points and data values are one-to-one in column charts.
     series.getDataPoints().get(i).clearFormat();

     // Get Y value.
     double yValue = series.getYValues().get(i).getDoubleValue();

     if (yValue < minValue)
     {
         minValue = yValue;
         minValueIndex = i;
     }

     if (yValue > maxValue)
     {
         maxValue = yValue;
         maxValueIndex = i;
     }
 }

 // Change colors of the max and min values.
 series.getDataPoints().get(minValueIndex).getFormat().getFill().setForeColor(Color.RED);
 series.getDataPoints().get(maxValueIndex).getFormat().getFill().setForeColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Charts.GetChartSeriesData.docx");
 
```
## 方法

| 方法 | 描述 |
| --- | --- |
| [get(int index)](#get-int) | 获取指定索引处的 X 值。 |
| [getCount()](#getCount) | 获取此集合中的项数。 |
| [getFormatCode()](#getFormatCode) | 获取应用于 X 值的格式代码。 |
| [iterator()](#iterator) | 返回一个枚举器对象。 |
| [set(int index, ChartXValue value)](#set-int-com.aspose.words.ChartXValue) | 设置指定索引处的 X 值。 |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | 设置应用于 X 值的格式代码。 |
### get(int index) {#get-int}
```
public ChartXValue get(int index)
```


获取指定索引处的 X 值。

 **Remarks:** 

空值表示为 **null**。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 索引 | int |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/) - The X value at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


获取此集合中的项数。

**Returns:**
int - 此集合中的项数。
### getFormatCode() {#getFormatCode}
```
public String getFormatCode()
```


获取应用于 X 值的格式代码。

 **Remarks:** 

数字格式用于更改值在图表中的显示方式。数字格式示例：

Number - "\#,\#\#0.00"

货币 - "\"$\"\#,\#\#0.00"

时间 - "[$-x-systime]h:mm:ss AM/PM"

日期 - "d/mm/yyyy"

百分比 - "0.00%"

分数 - "\# ?/?"

科学计数法 - "0.00E+00"

会计 - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

自定义颜色 - "[Red]-\#,\#\#0.0"

 **Examples:** 

展示如何使用图表数据的格式代码。

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Bubble chart.
 Shape shape = builder.insertChart(ChartType.BUBBLE, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();

 ChartSeries series = chart.getSeries().add(
         "Series1",
         new double[] { 1.0, 1.9, 2.45, 3.0 },
         new double[] { 1.0, -0.9, 1.82, 0.0 },
         new double[] { 2.0, 1.1, 2.95, 2.0 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowCategoryName(true);
 series.getDataLabels().setShowValue(true);
 series.getDataLabels().setShowBubbleSize(true);

 // Set data format codes.
 series.getXValues().setFormatCode("#,##0.0#");
 series.getYValues().setFormatCode("#,##0.0#;[Red]\\-#,##0.0#");
 series.getBubbleSizes().setFormatCode("#,##0.0#");

 doc.save(getArtifactsDir() + "Charts.FormatCode.docx");
 
```

**Returns:**
java.lang.String - 应用于 X 值的格式代码。
### iterator() {#iterator}
```
public Iterator iterator()
```


返回一个枚举器对象。

**Returns:**
java.util.Iterator
### set(int index, ChartXValue value) {#set-int-com.aspose.words.ChartXValue}
```
public void set(int index, ChartXValue value)
```


设置指定索引处的 X 值。

 **Remarks:** 

空值表示为 **null**。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 索引 | int |  |
| value | [ChartXValue](../../com.aspose.words/chartxvalue/) | 指定索引处的 X 值。 |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


设置应用于 X 值的格式代码。

 **Remarks:** 

数字格式用于更改值在图表中的显示方式。数字格式示例：

Number - "\#,\#\#0.00"

货币 - "\"$\"\#,\#\#0.00"

时间 - "[$-x-systime]h:mm:ss AM/PM"

日期 - "d/mm/yyyy"

百分比 - "0.00%"

分数 - "\# ?/?"

科学计数法 - "0.00E+00"

会计 - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

自定义颜色 - "[Red]-\#,\#\#0.0"

 **Examples:** 

展示如何使用图表数据的格式代码。

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Bubble chart.
 Shape shape = builder.insertChart(ChartType.BUBBLE, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();

 ChartSeries series = chart.getSeries().add(
         "Series1",
         new double[] { 1.0, 1.9, 2.45, 3.0 },
         new double[] { 1.0, -0.9, 1.82, 0.0 },
         new double[] { 2.0, 1.1, 2.95, 2.0 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowCategoryName(true);
 series.getDataLabels().setShowValue(true);
 series.getDataLabels().setShowBubbleSize(true);

 // Set data format codes.
 series.getXValues().setFormatCode("#,##0.0#");
 series.getYValues().setFormatCode("#,##0.0#;[Red]\\-#,##0.0#");
 series.getBubbleSizes().setFormatCode("#,##0.0#");

 doc.save(getArtifactsDir() + "Charts.FormatCode.docx");
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 应用于 X 值的格式代码。 |

