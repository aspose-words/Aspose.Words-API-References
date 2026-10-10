---
title: "ChartLegendEntryCollection"
linktitle: "ChartLegendEntryCollection"
second_title: "Aspose.Words Java için"
description: "Java'da grafik lejand girişlerinin bir koleksiyonunu temsil eder."
type: docs
weight: 81
url: /tr/java/com.aspose.words/chartlegendentrycollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartLegendEntryCollection implements Iterable
```

Grafik lejand girdilerinin bir koleksiyonunu temsil eder.

Daha fazla bilgi için, [ Working with Charts ][Working with Charts] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Grafik serileri için bir açıklama girişiyle nasıl çalışılacağını gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get(int index)](#get-int) | Belirtilen indeks için [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) döndürür. |
| [getCount()](#getCount) | Bu koleksiyondaki [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) sayısını döndürür. |
| [iterator()](#iterator) | Bir enumerator nesnesi döndürür. |
### get(int index) {#get-int}
```
public ChartLegendEntry get(int index)
```


Belirtilen indeks için [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) döndürür.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int |  |

**Returns:**
[ChartLegendEntry](../../com.aspose.words/chartlegendentry/) - [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) for the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Bu koleksiyondaki [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) sayısını döndürür.

**Returns:**
int - Bu koleksiyondaki [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) sayısı.
### iterator() {#iterator}
```
public Iterator iterator()
```


Bir enumerator nesnesi döndürür.

**Returns:**
java.util.Iterator
