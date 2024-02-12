---
title: ChartYValueCollection
linktitle: ChartYValueCollection
second_title: Aspose.Words for Java
description: Represents a collection of Y values for a chart series in Java.
type: docs
weight: 86
url: /java/com.aspose.words/chartyvaluecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartYValueCollection implements Iterable
```

Represents a collection of Y values for a chart series.

 **Remarks:** 

All items of the collection other than **null** must have the same [ChartYValue.getValueType()](../../com.aspose.words/chartyvalue/\#getValueType).

The collection allows only changing Y values. To add or insert new values to a chart series, or remove values, the appropriate methods of the [ChartSeries](../../com.aspose.words/chartseries/) class can be used.

 **Examples:** 

Shows how to get chart series data.

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
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int) | Gets the Y value at the specified index. |
| [getCount()](#getCount) | Gets the number of items in this collection. |
| [iterator()](#iterator) | Returns an enumerator object. |
| [set(int index, ChartYValue value)](#set-int-com.aspose.words.ChartYValue) | Sets the Y value at the specified index. |
### get(int index) {#get-int}
```
public ChartYValue get(int index)
```


Gets the Y value at the specified index.

 **Remarks:** 

Empty values are represented as **null**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/) - The Y value at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of items in this collection.

**Returns:**
int - The number of items in this collection.
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an enumerator object.

**Returns:**
java.util.Iterator
### set(int index, ChartYValue value) {#set-int-com.aspose.words.ChartYValue}
```
public void set(int index, ChartYValue value)
```


Sets the Y value at the specified index.

 **Remarks:** 

Empty values are represented as **null**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| value | [ChartYValue](../../com.aspose.words/chartyvalue/) | The Y value at the specified index. |

