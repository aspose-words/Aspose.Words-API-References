---
title: ChartDataLabelCollection.Separator
linktitle: Separator
articleTitle: Separator
second_title: Aspose.Words para .NET
description: Descubra la propiedad Separador de ChartDataLabelCollection. Personalice los separadores de etiquetas de datos para mejorar la claridad de sus gráficos, desde comas hasta saltos de línea.
type: docs
weight: 90
url: /es/net/aspose.words.drawing.charts/chartdatalabelcollection/separator/
---
## ChartDataLabelCollection.Separator property

Obtiene o establece el separador de cadena utilizado para las etiquetas de datos de toda la serie. El valor predeterminado es una coma, excepto para los gráficos circulares que muestran solo el nombre de la categoría y el porcentaje, en cuyo caso se debe utilizar un salto de línea en su lugar.

```csharp
public string Separator { get; set; }
```

## Observaciones

El valor definido para esta propiedad se puede anular para una etiqueta de datos individual mediante el uso de [`Separator`](../../chartdatalabel/separator/) propiedad.

## Ejemplos

Muestra cómo trabajar con etiquetas de datos de un gráfico de burbujas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.Series.Clear();

 // Agrega una serie personalizada con coordenadas X/Y y el diámetro de cada una de las burbujas.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { 2.9, 3.5, 1.1, 4.0, 4.0 },
    new[] { 1.9, 8.5, 2.1, 6.0, 1.5 },
    new[] { 9.0, 4.5, 2.5, 8.0, 5.0 });

// Habilite las etiquetas de datos y luego modifique su apariencia.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowBubbleSize = true;
dataLabels.ShowCategoryName = true;
dataLabels.ShowSeriesName = true;
dataLabels.Separator = " & ";

doc.Save(ArtifactsDir + "Charts.DataLabelsBubbleChart.docx");
```

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
