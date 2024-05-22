---
title: ChartXValue
linktitle: ChartXValue
second_title: Aspose.Words for Java
description: Represents an X value for a chart series in Java.
type: docs
weight: 87
url: /java/com.aspose.words/chartxvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartXValue
```

Represents an X value for a chart series.

 **Remarks:** 

This class contains a number of static methods for creating an X value of a particular type. The [getValueType()](../../com.aspose.words/chartxvalue/\#getValueType) property allows you to determine the type of an existing X value.

All non-null X values of a chart series must be of the same [ChartXValueType](../../com.aspose.words/chartxvaluetype/) type.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Gets a flag indicating whether the specified object is equal to the current X value object. |
| [fromDateTime(Date value)](#fromDateTime-java.util.Date) | Creates a [ChartXValue](../../com.aspose.words/chartxvalue/) instance of the [ChartXValueType.DATE\_TIME](../../com.aspose.words/chartxvaluetype/\#DATE-TIME) type. |
| [fromDouble(double value)](#fromDouble-double) | Creates a [ChartXValue](../../com.aspose.words/chartxvalue/) instance of the [ChartXValueType.DOUBLE](../../com.aspose.words/chartxvaluetype/\#DOUBLE) type. |
| [fromMultilevelValue(ChartMultilevelValue value)](#fromMultilevelValue-com.aspose.words.ChartMultilevelValue) | Creates a [ChartXValue](../../com.aspose.words/chartxvalue/) instance of the [ChartXValueType.MULTILEVEL](../../com.aspose.words/chartxvaluetype/\#MULTILEVEL) type. |
| [fromString(String value)](#fromString-java.lang.String) | Creates a [ChartXValue](../../com.aspose.words/chartxvalue/) instance of the [ChartXValueType.STRING](../../com.aspose.words/chartxvaluetype/\#STRING) type. |
| [fromTimeSpan(long value)](#fromTimeSpan-long) | Creates a [ChartXValue](../../com.aspose.words/chartxvalue/) instance of the [ChartXValueType.TIME](../../com.aspose.words/chartxvaluetype/\#TIME) type. |
| [getDateTimeValue()](#getDateTimeValue) | Gets the stored datetime value. |
| [getDoubleValue()](#getDoubleValue) | Gets the stored numeric value. |
| [getMultilevelValue()](#getMultilevelValue) | Gets the stored multilevel value. |
| [getStringValue()](#getStringValue) | Gets the stored string value. |
| [getTimeValue()](#getTimeValue) | Gets the stored time value. |
| [getValueType()](#getValueType) | Gets the type of the X value stored in the object. |
| [hashCode()](#hashCode) |  |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Gets a flag indicating whether the specified object is equal to the current X value object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromDateTime(Date value) {#fromDateTime-java.util.Date}
```
public static ChartXValue fromDateTime(Date value)
```


Creates a [ChartXValue](../../com.aspose.words/chartxvalue/) instance of the [ChartXValueType.DATE\_TIME](../../com.aspose.words/chartxvaluetype/\#DATE-TIME) type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.Date |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromDouble(double value) {#fromDouble-double}
```
public static ChartXValue fromDouble(double value)
```


Creates a [ChartXValue](../../com.aspose.words/chartxvalue/) instance of the [ChartXValueType.DOUBLE](../../com.aspose.words/chartxvaluetype/\#DOUBLE) type.

 **Examples:** 

Shows how to populate chart series with data.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder();

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series1 = chart.getSeries().get(0);

 // Clear X and Y values of the first series.
 series1.clearValues();

 // Populate the series with data.
 series1.add(ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0));
 series1.add(ChartXValue.fromDouble(5.0), ChartYValue.fromDouble(5.0));
 series1.add(ChartXValue.fromDouble(7.0), ChartYValue.fromDouble(11.0));
 series1.add(ChartXValue.fromDouble(9.0), ChartYValue.fromDouble(17.0));

 ChartSeries series2 = chart.getSeries().get(1);

 // Clear X and Y values of the second series.
 series2.clearValues();

 // Populate the series with data.
 series2.add(ChartXValue.fromDouble(2.0), ChartYValue.fromDouble(4.0));
 series2.add(ChartXValue.fromDouble(4.0), ChartYValue.fromDouble(7.0));
 series2.add(ChartXValue.fromDouble(6.0), ChartYValue.fromDouble(14.0));
 series2.add(ChartXValue.fromDouble(8.0), ChartYValue.fromDouble(7.0));

 doc.save(getArtifactsDir() + "Charts.PopulateChartWithData.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromMultilevelValue(ChartMultilevelValue value) {#fromMultilevelValue-com.aspose.words.ChartMultilevelValue}
```
public static ChartXValue fromMultilevelValue(ChartMultilevelValue value)
```


Creates a [ChartXValue](../../com.aspose.words/chartxvalue/) instance of the [ChartXValueType.MULTILEVEL](../../com.aspose.words/chartxvaluetype/\#MULTILEVEL) type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [ChartMultilevelValue](../../com.aspose.words/chartmultilevelvalue/) |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromString(String value) {#fromString-java.lang.String}
```
public static ChartXValue fromString(String value)
```


Creates a [ChartXValue](../../com.aspose.words/chartxvalue/) instance of the [ChartXValueType.STRING](../../com.aspose.words/chartxvaluetype/\#STRING) type.

 **Examples:** 

Shows how to add/remove chart data values.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromTimeSpan(long value) {#fromTimeSpan-long}
```
public static ChartXValue fromTimeSpan(long value)
```


Creates a [ChartXValue](../../com.aspose.words/chartxvalue/) instance of the [ChartXValueType.TIME](../../com.aspose.words/chartxvaluetype/\#TIME) type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | long |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### getDateTimeValue() {#getDateTimeValue}
```
public Date getDateTimeValue()
```


Gets the stored datetime value.

**Returns:**
java.util.Date - The stored datetime value.
### getDoubleValue() {#getDoubleValue}
```
public double getDoubleValue()
```


Gets the stored numeric value.

**Returns:**
double - The stored numeric value.
### getMultilevelValue() {#getMultilevelValue}
```
public ChartMultilevelValue getMultilevelValue()
```


Gets the stored multilevel value.

**Returns:**
[ChartMultilevelValue](../../com.aspose.words/chartmultilevelvalue/) - The stored multilevel value.
### getStringValue() {#getStringValue}
```
public String getStringValue()
```


Gets the stored string value.

**Returns:**
java.lang.String - The stored string value.
### getTimeValue() {#getTimeValue}
```
public long getTimeValue()
```


Gets the stored time value.

**Returns:**
long - The stored time value.
### getValueType() {#getValueType}
```
public int getValueType()
```


Gets the type of the X value stored in the object.

**Returns:**
int - The type of the X value stored in the object. The returned value is one of [ChartXValueType](../../com.aspose.words/chartxvaluetype/) constants.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
