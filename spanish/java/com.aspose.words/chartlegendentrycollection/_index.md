---
title: "ChartLegendEntryCollection"
linktitle: "ChartLegendEntryCollection"
second_title: "Aspose.Words para Java"
description: "Representa una colección de entradas de leyenda de gráfico en Java."
type: docs
weight: 81
url: /es/java/com.aspose.words/chartlegendentrycollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartLegendEntryCollection implements Iterable
```

Representa una colección de entradas de la leyenda del gráfico.

Para obtener más información, visite el artículo de documentación [ Working with Charts ][Working with Charts].

 **Examples:** 

Muestra cómo trabajar con una entrada de leyenda para series de gráficos.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [get(int index)](#get-int) | Devuelve [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) para el índice especificado. |
| [getCount()](#getCount) | Devuelve el número de [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) en esta colección. |
| [iterator()](#iterator) | Devuelve un objeto enumerador. |
### get(int index) {#get-int}
```
public ChartLegendEntry get(int index)
```


Devuelve [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) para el índice especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |

**Returns:**
[ChartLegendEntry](../../com.aspose.words/chartlegendentry/) - [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) for the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Devuelve el número de [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) en esta colección.

**Returns:**
int - El número de [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) en esta colección.
### iterator() {#iterator}
```
public Iterator iterator()
```


Devuelve un objeto enumerador.

**Returns:**
java.util.Iterator
