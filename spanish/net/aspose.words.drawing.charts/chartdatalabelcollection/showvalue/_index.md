---
title: ChartDataLabelCollection.ShowValue
linktitle: ShowValue
articleTitle: ShowValue
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad ShowValue de ChartDataLabelCollection mejora la visualización de sus datos al mostrar los valores de las series. ¡Optimice sus gráficos hoy mismo!
type: docs
weight: 170
url: /es/net/aspose.words.drawing.charts/chartdatalabelcollection/showvalue/
---
## ChartDataLabelCollection.ShowValue property

Permite especificar si se mostrarán valores en las etiquetas de datos de toda la serie. El valor predeterminado es`FALSO` .

```csharp
public bool ShowValue { get; set; }
```

## Observaciones

El valor definido para esta propiedad se puede anular para una etiqueta de datos individual mediante el uso de [`ShowValue`](../../chartdatalabel/showvalue/) propiedad.

## Ejemplos

Muestra cómo trabajar con etiquetas de datos de un gráfico circular.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.Series.Clear();

// Inserte una serie de gráficos personalizados con un nombre de categoría para cada uno de los sectores y su tabla de frecuencia.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// Habilite las etiquetas de datos que mostrarán tanto el porcentaje como la frecuencia de cada sector y modifique su apariencia.
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
