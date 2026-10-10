---
title: "ChartLegendEntryCollection"
linktitle: "ChartLegendEntryCollection"
second_title: "Aspose.Words für Java"
description: "Stellt eine Sammlung von Diagrammlegende‑Einträgen in Java dar."
type: docs
weight: 81
url: /de/java/com.aspose.words/chartlegendentrycollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartLegendEntryCollection implements Iterable
```

Stellt eine Sammlung von Einträgen der Diagrammlegende dar.

Weitere Informationen finden Sie im Dokumentationsartikel zu [ Working with Charts ][Working with Charts].

 **Examples:** 

Zeigt, wie man mit einem Legenden-Eintrag für Diagrammserien arbeitet.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get(int index)](#get-int) | Gibt [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) für den angegebenen Index zurück. |
| [getCount()](#getCount) | Gibt die Anzahl der [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) in dieser Sammlung zurück. |
| [iterator()](#iterator) | Gibt ein Enumerator‑Objekt zurück. |
### get(int index) {#get-int}
```
public ChartLegendEntry get(int index)
```


Gibt [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) für den angegebenen Index zurück.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |

**Returns:**
[ChartLegendEntry](../../com.aspose.words/chartlegendentry/) - [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) for the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Gibt die Anzahl der [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) in dieser Sammlung zurück.

**Returns:**
int - Die Anzahl der [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) in dieser Sammlung.
### iterator() {#iterator}
```
public Iterator iterator()
```


Gibt ein Enumerator‑Objekt zurück.

**Returns:**
java.util.Iterator
