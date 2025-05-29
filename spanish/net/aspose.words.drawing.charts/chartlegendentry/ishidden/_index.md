---
title: ChartLegendEntry.IsHidden
linktitle: IsHidden
articleTitle: IsHidden
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartLegendEntry IsHidden, que controla la visibilidad de la leyenda del gráfico sin esfuerzo. Mejore la presentación de sus datos con esta sencilla función de alternancia.
type: docs
weight: 20
url: /es/net/aspose.words.drawing.charts/chartlegendentry/ishidden/
---
## ChartLegendEntry.IsHidden property

Obtiene o establece un valor que indica si esta entrada está oculta en la leyenda del gráfico. El valor predeterminado es**FALSO** .

```csharp
public bool IsHidden { get; set; }
```

## Observaciones

Cuando se oculta una entrada de leyenda de gráfico, no afecta a la serie de gráfico o línea de tendencia correspondiente que aún se muestra en el gráfico.

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

* class [ChartLegendEntry](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
