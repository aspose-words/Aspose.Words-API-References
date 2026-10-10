---
title: "ChartYValue"
linktitle: "ChartYValue"
second_title: "Aspose.Words for Java"
description: "表示 Java 中图表系列的 Y 值。"
type: docs
weight: 97
url: /zh/java/com.aspose.words/chartyvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartYValue
```

表示图表系列的 Y 值。

 **Remarks:** 

此类包含多个用于创建特定类型 Y 值的静态方法。 [getValueType()](../../com.aspose.words/chartyvalue/\#getValueType) 属性允许您确定现有 Y 值的类型。

图表系列的所有非空 Y 值必须具有相同的 [ChartYValueType](../../com.aspose.words/chartyvaluetype/) 类型。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | 获取一个标志，指示指定对象是否等于当前 Y 值对象。 |
| [fromDateTime(Date value)](#fromDateTime-java.util.Date) | 创建一个 [ChartYValue](../../com.aspose.words/chartyvalue/) 实例，类型为 [ChartYValueType.DATE\_TIME](../../com.aspose.words/chartyvaluetype/\#DATE-TIME)。 |
| [fromDouble(double value)](#fromDouble-double) | 创建一个 [ChartYValue](../../com.aspose.words/chartyvalue/) 实例，类型为 [ChartYValueType.DOUBLE](../../com.aspose.words/chartyvaluetype/\#DOUBLE)。 |
| [fromTimeSpan(long value)](#fromTimeSpan-long) | 创建一个 [ChartYValue](../../com.aspose.words/chartyvalue/) 实例，类型为 [ChartYValueType.TIME](../../com.aspose.words/chartyvaluetype/\#TIME)。 |
| [getDateTimeValue()](#getDateTimeValue) | 获取存储的日期时间值。 |
| [getDoubleValue()](#getDoubleValue) | 获取存储的数值。 |
| [getTimeValue()](#getTimeValue) | 获取存储的时间值。 |
| [getValueType()](#getValueType) | 获取对象中存储的 Y 值的类型。 |
| [hashCode()](#hashCode) |  |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


获取一个标志，指示指定对象是否等于当前 Y 值对象。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromDateTime(Date value) {#fromDateTime-java.util.Date}
```
public static ChartYValue fromDateTime(Date value)
```


创建一个 [ChartYValue](../../com.aspose.words/chartyvalue/) 实例，类型为 [ChartYValueType.DATE\_TIME](../../com.aspose.words/chartyvaluetype/\#DATE-TIME)。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | java.util.Date |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
### fromDouble(double value) {#fromDouble-double}
```
public static ChartYValue fromDouble(double value)
```


创建一个 [ChartYValue](../../com.aspose.words/chartyvalue/) 实例，类型为 [ChartYValueType.DOUBLE](../../com.aspose.words/chartyvaluetype/\#DOUBLE)。

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
[ChartYValue](../../com.aspose.words/chartyvalue/)
### fromTimeSpan(long value) {#fromTimeSpan-long}
```
public static ChartYValue fromTimeSpan(long value)
```


创建一个 [ChartYValue](../../com.aspose.words/chartyvalue/) 实例，类型为 [ChartYValueType.TIME](../../com.aspose.words/chartyvaluetype/\#TIME)。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | long |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
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


获取对象中存储的 Y 值的类型。

**Returns:**
int - 对象中存储的 Y 值的类型。返回值是 [ChartYValueType](../../com.aspose.words/chartyvaluetype/) 常量之一。
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
