---
title: "AxisGroup"
linktitle: "AxisGroup"
second_title: "Aspose.Words for Java"
description: "表示 Java 中图表坐标轴组的类型。"
type: docs
weight: 27
url: /zh/java/com.aspose.words/axisgroup/
---

**Inheritance:**
java.lang.Object
```
public class AxisGroup
```

表示图表坐标轴组的类型。

 **Examples:** 

展示如何使用图表的次要坐标轴。

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 250.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();

 // Delete default generated series.
 series.clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 series.add("Series 1 of primary series group", categories, new double[] { 2.0, 3.0, 4.0 });
 series.add("Series 2 of primary series group", categories, new double[] { 5.0, 2.0, 3.0 });

 // Create an additional series group, also of the line type.
 ChartSeriesGroup newSeriesGroup = chart.getSeriesGroups().add(ChartSeriesType.LINE);
 // Specify the use of secondary axes for the new series group.
 newSeriesGroup.setAxisGroup(AxisGroup.SECONDARY);
 // Hide the secondary X axis.
 newSeriesGroup.getAxisX().setHidden(true);
 // Define title of the secondary Y axis.
 newSeriesGroup.getAxisY().getTitle().setShow(true);
 newSeriesGroup.getAxisY().getTitle().setText("Secondary Y axis");

 Assert.assertEquals(ChartSeriesType.LINE, newSeriesGroup.getSeriesType());

 // Add a series to the new series group.
 ChartSeries series3 =
         newSeriesGroup.getSeries().add("Series of secondary series group", categories, new double[] { 13.0, 11.0, 16.0 });
 series3.getFormat().getStroke().setWeight(3.5);

 doc.save(getArtifactsDir() + "Charts.SecondaryAxis.docx");
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [PRIMARY](#PRIMARY) | 指定主坐标轴组。 |
| [SECONDARY](#SECONDARY) | 指定次坐标轴组。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String axisGroupName)](#fromName-java.lang.String) |  |
| [getName(int axisGroup)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int axisGroup)](#toString-int) |  |
### PRIMARY {#PRIMARY}
```
public static int PRIMARY
```


指定主坐标轴组。

### SECONDARY {#SECONDARY}
```
public static int SECONDARY
```


指定次坐标轴组。

### length {#length}
```
public static int length
```


### fromName(String axisGroupName) {#fromName-java.lang.String}
```
public static int fromName(String axisGroupName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| axisGroupName | java.lang.String |  |

**Returns:**
int
### getName(int axisGroup) {#getName-int}
```
public static String getName(int axisGroup)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| axisGroup | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int axisGroup) {#toString-int}
```
public static String toString(int axisGroup)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| axisGroup | int |  |

**Returns:**
java.lang.String
