---
title: "ChartLegendEntryCollection"
linktitle: "ChartLegendEntryCollection"
second_title: "Aspose.Words pour Java"
description: "Représente une collection d'entrées de légende de graphique en Java."
type: docs
weight: 81
url: /fr/java/com.aspose.words/chartlegendentrycollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartLegendEntryCollection implements Iterable
```

Représente une collection d'entrées de légende de graphique.

Pour en savoir plus, consultez l'article de documentation [ Working with Charts ][Working with Charts].

 **Examples:** 

Montre comment travailler avec une entrée de légende pour les séries du graphique.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [get(int index)](#get-int) | Renvoie [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) pour l'index spécifié. |
| [getCount()](#getCount) | Renvoie le nombre de [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) dans cette collection. |
| [iterator()](#iterator) | Renvoie un objet énumérateur. |
### get(int index) {#get-int}
```
public ChartLegendEntry get(int index)
```


Renvoie [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) pour l'index spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[ChartLegendEntry](../../com.aspose.words/chartlegendentry/) - [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) for the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Renvoie le nombre de [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) dans cette collection.

**Returns:**
int - Le nombre de [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) dans cette collection.
### iterator() {#iterator}
```
public Iterator iterator()
```


Renvoie un objet énumérateur.

**Returns:**
java.util.Iterator
