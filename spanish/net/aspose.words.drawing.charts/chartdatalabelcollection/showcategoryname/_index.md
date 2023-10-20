---
title: ChartDataLabelCollection.ShowCategoryName
linktitle: ShowCategoryName
articleTitle: ShowCategoryName
second_title: Aspose.Words para .NET
description: ChartDataLabelCollection ShowCategoryName propiedad. Permite especificar si el nombre de la categoría se mostrará para las etiquetas de datos de toda la serie. El valor predeterminado esFALSO  en C#.
type: docs
weight: 80
url: /es/net/aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/
---
## ChartDataLabelCollection.ShowCategoryName property

Permite especificar si el nombre de la categoría se mostrará para las etiquetas de datos de toda la serie. El valor predeterminado es`FALSO` .

```csharp
public bool ShowCategoryName { get; set; }
```

## Observaciones

El valor definido para esta propiedad se puede anular para una etiqueta de datos individual usando the [`ShowCategoryName`](../../chartdatalabel/showcategoryname/) propiedad.

## Ejemplos

Muestra cómo trabajar con etiquetas de datos de un gráfico de burbujas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// Borra la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.Series.Clear();

// Agrega una serie personalizada con coordenadas X/Y y diámetro de cada una de las burbujas.
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

### Ver también

* class [ChartDataLabelCollection](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
