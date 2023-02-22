---
title: ChartDataLabelCollection.ShowSeriesName
second_title: Referencia de API de Aspose.Words para .NET
description: ChartDataLabelCollection propiedad. Devuelve o establece un valor booleano para indicar el comportamiento de visualización del nombre de la serie para las etiquetas de datos de toda la serie.  Verdaderopara mostrar el nombre de la serie. Falso esconder. Por defecto falso .
type: docs
weight: 110
url: /es/net/aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/
---
## ChartDataLabelCollection.ShowSeriesName property

Devuelve o establece un valor booleano para indicar el comportamiento de visualización del nombre de la serie para las etiquetas de datos de toda la serie.  **Verdadero**para mostrar el nombre de la serie. **Falso** esconder. Por defecto **falso** .

```csharp
public bool ShowSeriesName { get; set; }
```

### Observaciones

El valor definido para esta propiedad se puede anular para una etiqueta de datos individual con el uso de [`ShowSeriesName`](../../chartdatalabel/showseriesname/) propiedad.

### Ejemplos

Muestra cómo trabajar con etiquetas de datos de un gráfico de burbujas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.Series.Clear();

  // Agregue una serie personalizada con las coordenadas X/Y y el diámetro de cada una de las burbujas.
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
* espacio de nombres [Aspose.Words.Drawing.Charts](../../chartdatalabelcollection/)
* asamblea [Aspose.Words](../../../)


