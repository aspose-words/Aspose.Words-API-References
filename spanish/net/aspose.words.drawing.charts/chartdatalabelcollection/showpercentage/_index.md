---
title: ChartDataLabelCollection.ShowPercentage
linktitle: ShowPercentage
articleTitle: ShowPercentage
second_title: Aspose.Words para .NET
description: ChartDataLabelCollection ShowPercentage propiedad. Permite especificar si se mostrará el valor porcentual para las etiquetas de datos de toda la serie. El valor predeterminado esFALSO . Se aplica sólo a gráficos circulares en C#.
type: docs
weight: 120
url: /es/net/aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/
---
## ChartDataLabelCollection.ShowPercentage property

Permite especificar si se mostrará el valor porcentual para las etiquetas de datos de toda la serie. El valor predeterminado es`FALSO` . Se aplica sólo a gráficos circulares.

```csharp
public bool ShowPercentage { get; set; }
```

## Observaciones

El valor definido para esta propiedad se puede anular para una etiqueta de datos individual usando the [`ShowPercentage`](../../chartdatalabel/showpercentage/) propiedad.

## Ejemplos

Muestra cómo trabajar con etiquetas de datos de un gráfico circular.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// Borra la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.Series.Clear();

// Inserta una serie de gráficos personalizados con un nombre de categoría para cada uno de los sectores y su tabla de frecuencia.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// Habilita etiquetas de datos que mostrarán tanto el porcentaje como la frecuencia de cada sector, y modificarán su apariencia.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowLeaderLines = true;
dataLabels.ShowLegendKey = true;
dataLabels.ShowPercentage = true;
dataLabels.ShowValue = true;
dataLabels.Separator = "; ";

doc.Save(ArtifactsDir + "Charts.DataLabelsPieChart.docx");
```

### Ver también

* class [ChartDataLabelCollection](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
