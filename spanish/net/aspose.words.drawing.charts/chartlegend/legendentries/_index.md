---
title: ChartLegend.LegendEntries
linktitle: LegendEntries
articleTitle: LegendEntries
second_title: Aspose.Words para .NET
description: Explore la propiedad LegendEntries de ChartLegend para acceder a una colección completa de entradas de leyenda para todas las series y líneas de tendencia en su gráfico.
type: docs
weight: 30
url: /es/net/aspose.words.drawing.charts/chartlegend/legendentries/
---
## ChartLegend.LegendEntries property

Devuelve una colección de entradas de leyenda para todas las series y líneas de tendencia del gráfico principal.

```csharp
public ChartLegendEntryCollection LegendEntries { get; }
```

## Ejemplos

Muestra cómo trabajar con una entrada de leyenda para series de gráficos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "AW Category 1", "AW Category 2" };

ChartSeries series1 = series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });
series.Add("Series 3", categories, new double[] { 5, 6 });
series.Add("Series 4", categories, new double[] { 0, 0 });

ChartLegendEntryCollection legendEntries = chart.Legend.LegendEntries;
legendEntries[3].IsHidden = true;

doc.Save(ArtifactsDir + "Charts.LegendEntries.docx");
```

### Ver también

* class [ChartLegendEntryCollection](../../chartlegendentrycollection/)
* class [ChartLegend](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
