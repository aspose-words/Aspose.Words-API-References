---
title: "ChartLegendEntryCollection"
linktitle: "ChartLegendEntryCollection"
second_title: "Aspose.Words per Java"
description: "Rappresenta una raccolta di voci della legenda del grafico in Java."
type: docs
weight: 81
url: /it/java/com.aspose.words/chartlegendentrycollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartLegendEntryCollection implements Iterable
```

Rappresenta una raccolta di voci della legenda del grafico.

Per saperne di più, visita l'articolo di documentazione [ Working with Charts ][Working with Charts].

 **Examples:** 

Mostra come lavorare con una voce della legenda per le serie del grafico.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get(int index)](#get-int) | Restituisce [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) per l'indice specificato. |
| [getCount()](#getCount) | Restituisce il numero di [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) in questa raccolta. |
| [iterator()](#iterator) | Restituisce un oggetto enumeratore. |
### get(int index) {#get-int}
```
public ChartLegendEntry get(int index)
```


Restituisce [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) per l'indice specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |

**Returns:**
[ChartLegendEntry](../../com.aspose.words/chartlegendentry/) - [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) for the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Restituisce il numero di [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) in questa raccolta.

**Returns:**
int - Il numero di [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) in questa raccolta.
### iterator() {#iterator}
```
public Iterator iterator()
```


Restituisce un oggetto enumeratore.

**Returns:**
java.util.Iterator
