---
title: "BubbleSizeCollection"
linktitle: "BubbleSizeCollection"
second_title: "Aspose.Words for Java"
description: "表示 Java 中图表系列的气泡大小集合。"
type: docs
weight: 50
url: /zh/java/com.aspose.words/bubblesizecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BubbleSizeCollection implements Iterable
```

表示图表系列的气泡大小集合。

 **Remarks:** 

该集合仅允许更改气泡大小。要向图表系列添加或插入新值，或删除值，可使用 [ChartSeries](../../com.aspose.words/chartseries/) 类的相应方法。

空的气泡大小值表示为 double\#NA\_N.NA\_N。
## 方法

| 方法 | 描述 |
| --- | --- |
| [get(int index)](#get-int) | 获取指定索引处的气泡大小值。 |
| [getCount()](#getCount) | 获取此集合中的项数。 |
| [getFormatCode()](#getFormatCode) | 获取应用于气泡大小的格式代码。 |
| [iterator()](#iterator) | 返回一个枚举器对象。 |
| [set(int index, double value)](#set-int-double) | 在指定索引处设置气泡大小值。 |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | 设置应用于气泡大小的格式代码。 |
### get(int index) {#get-int}
```
public double get(int index)
```


获取指定索引处的气泡大小值。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 索引 | int |  |

**Returns:**
double - 指定索引处的气泡大小值。
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


获取应用于气泡大小的格式代码。

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
java.lang.String - 应用于气泡大小的格式代码。
### iterator() {#iterator}
```
public Iterator iterator()
```


返回一个枚举器对象。

**Returns:**
java.util.Iterator
### set(int index, double value) {#set-int-double}
```
public void set(int index, double value)
```


在指定索引处设置气泡大小值。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 索引 | int |  |
| value | double | 指定索引处的气泡大小值。 |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


设置应用于气泡大小的格式代码。

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
| value | java.lang.String | 应用于气泡大小的格式代码。 |

