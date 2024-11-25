---
title: BubbleSizeCollection
linktitle: BubbleSizeCollection
second_title: Aspose.Words for Java
description: Represents a collection of bubble sizes for a chart series in Java.
type: docs
weight: 49
url: /java/com.aspose.words/bubblesizecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BubbleSizeCollection implements Iterable
```

Represents a collection of bubble sizes for a chart series.

 **Remarks:** 

The collection allows only changing bubble sizes. To add or insert new values to a chart series, or remove values, the appropriate methods of the [ChartSeries](../../com.aspose.words/chartseries/) class can be used.

Empty bubble size values are represented as double\#NA\_N.NA\_N.
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int) | Gets the bubble size value at the specified index. |
| [getCount()](#getCount) | Gets the number of items in this collection. |
| [getFormatCode()](#getFormatCode) | Gets the format code applied to the bubble sizes. |
| [iterator()](#iterator) | Returns an enumerator object. |
| [set(int index, double value)](#set-int-double) | Sets the bubble size value at the specified index. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | Sets the format code applied to the bubble sizes. |
### get(int index) {#get-int}
```
public double get(int index)
```


Gets the bubble size value at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
double - The bubble size value at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of items in this collection.

**Returns:**
int - The number of items in this collection.
### getFormatCode() {#getFormatCode}
```
public String getFormatCode()
```


Gets the format code applied to the bubble sizes.

 **Remarks:** 

Number formatting is used to change the way values appears in the chart. The examples of number formats:

Number - "\#,\#\#0.00"

Currency - "\\"$\\"\#,\#\#0.00"

Time - "[$-x-systime]h:mm:ss AM/PM"

Date - "d/mm/yyyy"

Percentage - "0.00%"

Fraction - "\# ?/?"

Scientific - "0.00E+00"

Accounting - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

Custom with color - "[Red]-\#,\#\#0.0"

 **Examples:** 

Shows how to work with the format code of the chart data.

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
java.lang.String - The format code applied to the bubble sizes.
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an enumerator object.

**Returns:**
java.util.Iterator
### set(int index, double value) {#set-int-double}
```
public void set(int index, double value)
```


Sets the bubble size value at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| value | double | The bubble size value at the specified index. |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


Sets the format code applied to the bubble sizes.

 **Remarks:** 

Number formatting is used to change the way values appears in the chart. The examples of number formats:

Number - "\#,\#\#0.00"

Currency - "\\"$\\"\#,\#\#0.00"

Time - "[$-x-systime]h:mm:ss AM/PM"

Date - "d/mm/yyyy"

Percentage - "0.00%"

Fraction - "\# ?/?"

Scientific - "0.00E+00"

Accounting - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

Custom with color - "[Red]-\#,\#\#0.0"

 **Examples:** 

Shows how to work with the format code of the chart data.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The format code applied to the bubble sizes. |

