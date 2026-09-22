---
title: "ChartAxisCollection"
linktitle: "ChartAxisCollection"
second_title: "Aspose.Words لـ Java"
description: "يمثل مجموعة من محاور المخطط في Java."
type: docs
weight: 68
url: /ar/java/com.aspose.words/chartaxiscollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartAxisCollection implements Iterable
```

يمثل مجموعة من محاور المخطط.

 **Examples:** 

يوضح كيفية العمل مع مجموعة المحاور.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [get(int index)](#get-int) | يحصل على المحور عند الفهرس المحدد. |
| [getCount()](#getCount) | يحصل على عدد المحاور في هذه المجموعة. |
| [iterator()](#iterator) | يرجع كائن عداد. |
### get(int index) {#get-int}
```
public ChartAxis get(int index)
```


يحصل على المحور عند الفهرس المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int |  |

**Returns:**
[ChartAxis](../../com.aspose.words/chartaxis/) - The axis at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


يحصل على عدد المحاور في هذه المجموعة.

**Returns:**
int - عدد المحاور في هذه المجموعة.
### iterator() {#iterator}
```
public Iterator iterator()
```


يرجع كائن عداد.

**Returns:**
java.util.Iterator
