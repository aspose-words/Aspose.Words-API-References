---
title: ChartAxisCollection
linktitle: ChartAxisCollection
second_title: Aspose.Words for Java
description: Represents a collection of chart axes in Java.
type: docs
weight: 58
url: /java/com.aspose.words/chartaxiscollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartAxisCollection implements Iterable
```

Represents a collection of chart axes.

 **Examples:** 

Shows how to work with axes collection.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Hide the major grid lines on the primary and secondary Y axes.
 for (ChartAxis axis : chart.getAxes())
 {
     if (axis.getType() == ChartAxisType.VALUE)
         axis.hasMajorGridlines(false);
 }

 doc.save(getArtifactsDir() + "Charts.AxisCollection.docx");
 
```
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int) | Gets the axis at the specified index. |
| [getCount()](#getCount) | Gets the number of axes in this collection. |
| [iterator()](#iterator) | Returns an enumerator object. |
### get(int index) {#get-int}
```
public ChartAxis get(int index)
```


Gets the axis at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[ChartAxis](../../com.aspose.words/chartaxis/) - The axis at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of axes in this collection.

**Returns:**
int - The number of axes in this collection.
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an enumerator object.

**Returns:**
java.util.Iterator
