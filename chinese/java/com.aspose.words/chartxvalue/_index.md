---
title: "ChartXValue"
linktitle: "ChartXValue"
second_title: "Aspose.Words for Java"
description: "表示 Java 中图表系列的 X 值。"
type: docs
weight: 94
url: /zh/java/com.aspose.words/chartxvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartXValue
```

表示图表系列的 X 值。

 **Remarks:** 

此类包含多个用于创建特定类型 X 值的静态方法。 [getValueType()](../../com.aspose.words/chartxvalue/\#getValueType) 属性允许您确定现有 X 值的类型。

图表系列的所有非空 X 值必须具有相同的 [ChartXValueType](../../com.aspose.words/chartxvaluetype/) 类型。

 **Examples:** 

展示如何使用数据填充图表系列。

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series1 = chart.getSeries().get(0);

 // Clear X and Y values of the first series.
 series1.clearValues();

 // Populate the series with data.
 series1.add(ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0), 10.0);
 series1.add(ChartXValue.fromDouble(5.0), ChartYValue.fromDouble(5.0));
 series1.add(ChartXValue.fromDouble(7.0), ChartYValue.fromDouble(11.0));
 series1.add(ChartXValue.fromDouble(9.0));

 ChartSeries series2 = chart.getSeries().get(1);

 // Clear X and Y values of the second series.
 series2.clear();

 // Populate the series with data.
 series2.add(ChartXValue.fromDouble(2.0), ChartYValue.fromDouble(4.0));
 series2.add(ChartXValue.fromDouble(4.0), ChartYValue.fromDouble(7.0));
 series2.add(ChartXValue.fromDouble(6.0), ChartYValue.fromDouble(14.0));
 series2.add(ChartXValue.fromDouble(8.0), ChartYValue.fromDouble(7.0));

 doc.save(getArtifactsDir() + "Charts.PopulateChartWithData.docx");
 
```
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | 获取一个标志，指示指定的对象是否等于当前的 X 值对象。 |
| [fromDateTime(Date value)](#fromDateTime-java.util.Date) | 创建一个 [ChartXValue](../../com.aspose.words/chartxvalue/) 实例，类型为 [ChartXValueType.DATE\_TIME](../../com.aspose.words/chartxvaluetype/\#DATE-TIME)。 |
| [fromDouble(double value)](#fromDouble-double) | 创建一个 [ChartXValue](../../com.aspose.words/chartxvalue/) 实例，类型为 [ChartXValueType.DOUBLE](../../com.aspose.words/chartxvaluetype/\#DOUBLE)。 |
| [fromMultilevelValue(ChartMultilevelValue value)](#fromMultilevelValue-com.aspose.words.ChartMultilevelValue) | 创建一个 [ChartXValue](../../com.aspose.words/chartxvalue/) 实例，类型为 [ChartXValueType.MULTILEVEL](../../com.aspose.words/chartxvaluetype/\#MULTILEVEL)。 |
| [fromString(String value)](#fromString-java.lang.String) | 创建一个 [ChartXValue](../../com.aspose.words/chartxvalue/) 实例，类型为 [ChartXValueType.STRING](../../com.aspose.words/chartxvaluetype/\#STRING)。 |
| [fromTimeSpan(long value)](#fromTimeSpan-long) | 创建一个 [ChartXValue](../../com.aspose.words/chartxvalue/) 实例，类型为 [ChartXValueType.TIME](../../com.aspose.words/chartxvaluetype/\#TIME)。 |
| [getDateTimeValue()](#getDateTimeValue) | 获取存储的日期时间值。 |
| [getDoubleValue()](#getDoubleValue) | 获取存储的数值。 |
| [getMultilevelValue()](#getMultilevelValue) | 获取存储的多层级值。 |
| [getStringValue()](#getStringValue) | 获取存储的字符串值。 |
| [getTimeValue()](#getTimeValue) | 获取存储的时间值。 |
| [getValueType()](#getValueType) | 获取对象中存储的 X 值的类型。 |
| [hashCode()](#hashCode) |  |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


获取一个标志，指示指定的对象是否等于当前的 X 值对象。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromDateTime(Date value) {#fromDateTime-java.util.Date}
```
public static ChartXValue fromDateTime(Date value)
```


创建一个 [ChartXValue](../../com.aspose.words/chartxvalue/) 实例，类型为 [ChartXValueType.DATE\_TIME](../../com.aspose.words/chartxvaluetype/\#DATE-TIME)。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | java.util.Date |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromDouble(double value) {#fromDouble-double}
```
public static ChartXValue fromDouble(double value)
```


创建一个 [ChartXValue](../../com.aspose.words/chartxvalue/) 实例，类型为 [ChartXValueType.DOUBLE](../../com.aspose.words/chartxvaluetype/\#DOUBLE)。

 **Examples:** 

展示如何使用数据填充图表系列。

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series1 = chart.getSeries().get(0);

 // Clear X and Y values of the first series.
 series1.clearValues();

 // Populate the series with data.
 series1.add(ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0), 10.0);
 series1.add(ChartXValue.fromDouble(5.0), ChartYValue.fromDouble(5.0));
 series1.add(ChartXValue.fromDouble(7.0), ChartYValue.fromDouble(11.0));
 series1.add(ChartXValue.fromDouble(9.0));

 ChartSeries series2 = chart.getSeries().get(1);

 // Clear X and Y values of the second series.
 series2.clear();

 // Populate the series with data.
 series2.add(ChartXValue.fromDouble(2.0), ChartYValue.fromDouble(4.0));
 series2.add(ChartXValue.fromDouble(4.0), ChartYValue.fromDouble(7.0));
 series2.add(ChartXValue.fromDouble(6.0), ChartYValue.fromDouble(14.0));
 series2.add(ChartXValue.fromDouble(8.0), ChartYValue.fromDouble(7.0));

 doc.save(getArtifactsDir() + "Charts.PopulateChartWithData.docx");
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | double |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromMultilevelValue(ChartMultilevelValue value) {#fromMultilevelValue-com.aspose.words.ChartMultilevelValue}
```
public static ChartXValue fromMultilevelValue(ChartMultilevelValue value)
```


创建一个 [ChartXValue](../../com.aspose.words/chartxvalue/) 实例，类型为 [ChartXValueType.MULTILEVEL](../../com.aspose.words/chartxvaluetype/\#MULTILEVEL)。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | [ChartMultilevelValue](../../com.aspose.words/chartmultilevelvalue/) |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromString(String value) {#fromString-java.lang.String}
```
public static ChartXValue fromString(String value)
```


创建一个 [ChartXValue](../../com.aspose.words/chartxvalue/) 实例，类型为 [ChartXValueType.STRING](../../com.aspose.words/chartxvaluetype/\#STRING)。

 **Examples:** 

展示如何添加/删除图表数据值。

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder();

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries department1Series = chart.getSeries().get(0);
 ChartSeries department2Series = chart.getSeries().get(1);

 // Remove the first value in the both series.
 department1Series.remove(0);
 department2Series.remove(0);

 // Add new values to the both series.
 ChartXValue newXCategory = ChartXValue.fromString("Q1, 2023");
 department1Series.add(newXCategory, ChartYValue.fromDouble(10.3));
 department2Series.add(newXCategory, ChartYValue.fromDouble(5.7));

 doc.save(getArtifactsDir() + "Charts.ChartDataValues.docx");
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromTimeSpan(long value) {#fromTimeSpan-long}
```
public static ChartXValue fromTimeSpan(long value)
```


创建一个 [ChartXValue](../../com.aspose.words/chartxvalue/) 实例，类型为 [ChartXValueType.TIME](../../com.aspose.words/chartxvaluetype/\#TIME)。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | long |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### getDateTimeValue() {#getDateTimeValue}
```
public Date getDateTimeValue()
```


获取存储的日期时间值。

**Returns:**
java.util.Date - 存储的日期时间值。
### getDoubleValue() {#getDoubleValue}
```
public double getDoubleValue()
```


获取存储的数值。

**Returns:**
double - 存储的数值。
### getMultilevelValue() {#getMultilevelValue}
```
public ChartMultilevelValue getMultilevelValue()
```


获取存储的多层级值。

**Returns:**
[ChartMultilevelValue](../../com.aspose.words/chartmultilevelvalue/) - The stored multilevel value.
### getStringValue() {#getStringValue}
```
public String getStringValue()
```


获取存储的字符串值。

**Returns:**
java.lang.String - 存储的字符串值。
### getTimeValue() {#getTimeValue}
```
public long getTimeValue()
```


获取存储的时间值。

**Returns:**
long - 存储的时间值。
### getValueType() {#getValueType}
```
public int getValueType()
```


获取对象中存储的 X 值的类型。

**Returns:**
int - 对象中存储的 X 值的类型。返回的值是 [ChartXValueType](../../com.aspose.words/chartxvaluetype/) 常量之一。
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
