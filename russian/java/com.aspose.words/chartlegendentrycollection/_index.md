---
title: "ChartLegendEntryCollection"
linktitle: "ChartLegendEntryCollection"
second_title: "Aspose.Words для Java"
description: "Представляет коллекцию элементов легенды диаграммы в Java."
type: docs
weight: 81
url: /ru/java/com.aspose.words/chartlegendentrycollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartLegendEntryCollection implements Iterable
```

Представляет коллекцию записей легенды диаграммы.

Чтобы узнать больше, посетите статью документации [ Working with Charts ][Working with Charts].

 **Examples:** 

Показывает, как работать с элементом легенды для рядов диаграммы.

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
## Методы

| Метод | Описание |
| --- | --- |
| [get(int index)](#get-int) | Возвращает [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) для указанного индекса. |
| [getCount()](#getCount) | Возвращает количество [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) в этой коллекции. |
| [iterator()](#iterator) | Возвращает объект перечислителя. |
### get(int index) {#get-int}
```
public ChartLegendEntry get(int index)
```


Возвращает [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) для указанного индекса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int |  |

**Returns:**
[ChartLegendEntry](../../com.aspose.words/chartlegendentry/) - [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) for the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Возвращает количество [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) в этой коллекции.

**Returns:**
int - количество [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) в этой коллекции.
### iterator() {#iterator}
```
public Iterator iterator()
```


Возвращает объект перечислителя.

**Returns:**
java.util.Iterator
