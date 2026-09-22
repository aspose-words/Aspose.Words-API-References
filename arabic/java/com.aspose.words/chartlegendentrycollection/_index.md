---
title: "ChartLegendEntryCollection"
linktitle: "ChartLegendEntryCollection"
second_title: "Aspose.Words لـ Java"
description: "يمثل مجموعة من مدخلات وسيلة إيضاح المخطط في Java."
type: docs
weight: 81
url: /ar/java/com.aspose.words/chartlegendentrycollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartLegendEntryCollection implements Iterable
```

يمثل مجموعة من مدخلات وسيلة إيضاح المخطط.

للتعرف على المزيد، زر مقالة توثيق [ Working with Charts ][Working with Charts].

 **Examples:** 

يوضح كيفية التعامل مع مدخل وسيلة إيضاح لسلسلة المخطط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();
 series.clear();

 String[] categories = new String[] { "AW Category 1", "AW Category 2" };

 ChartSeries series1 = series.add("Series 1", categories, new double[] { 1.0, 2.0 });
 series.add("Series 2", categories, new double[] { 3.0, 4.0 });
 series.add("Series 3", categories, new double[] { 5.0, 6.0 });
 series.add("Series 4", categories, new double[] { 0.0, 0.0 });

 ChartLegendEntryCollection legendEntries = chart.getLegend().getLegendEntries();
 legendEntries.get(3).isHidden(true);

 doc.save(getArtifactsDir() + "Charts.LegendEntries.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [get(int index)](#get-int) | يرجع [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) للفهرس المحدد. |
| [getCount()](#getCount) | يرجع عدد [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) في هذه المجموعة. |
| [iterator()](#iterator) | يرجع كائن عداد. |
### get(int index) {#get-int}
```
public ChartLegendEntry get(int index)
```


يرجع [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) للفهرس المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int |  |

**Returns:**
[ChartLegendEntry](../../com.aspose.words/chartlegendentry/) - [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) for the specified index.
### getCount() {#getCount}
```
public int getCount()
```


يرجع عدد [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) في هذه المجموعة.

**Returns:**
int - عدد [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) في هذه المجموعة.
### iterator() {#iterator}
```
public Iterator iterator()
```


يرجع كائن عداد.

**Returns:**
java.util.Iterator
