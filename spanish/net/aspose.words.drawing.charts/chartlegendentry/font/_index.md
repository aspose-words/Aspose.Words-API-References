---
title: ChartLegendEntry.Font
second_title: Referencia de API de Aspose.Words para .NET
description: ChartLegendEntry propiedad. Proporciona acceso al formato de fuente de esta entrada de leyenda.
type: docs
weight: 10
url: /es/net/aspose.words.drawing.charts/chartlegendentry/font/
---
## ChartLegendEntry.Font property

Proporciona acceso al formato de fuente de esta entrada de leyenda.

```csharp
public Font Font { get; }
```

### Ejemplos

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

foreach (ChartLegendEntry legendEntry in legendEntries)
    legendEntry.Font.Size = 12;

series1.LegendEntry.Font.Italic = true;

doc.Save(ArtifactsDir + "Charts.LegendEntries.docx");
```

### Ver también

* class [Font](../../../aspose.words/font/)
* class [ChartLegendEntry](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../chartlegendentry/)
* asamblea [Aspose.Words](../../../)


