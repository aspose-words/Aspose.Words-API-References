---
title: ChartSeries.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words para .NET
description: Optimice sus gráficos con el método ChartSeries Clear. Elimine fácilmente los valores de datos y restablezca el formato para una apariencia más limpia y profesional.
type: docs
weight: 170
url: /es/net/aspose.words.drawing.charts/chartseries/clear/
---
## ChartSeries.Clear method

Elimina todos los valores de datos de la serie gráfica. Se borra el formato de todos los puntos de datos y etiquetas de datos.

```csharp
public void Clear()
```

## Ejemplos

Muestra cómo rellenar series de gráficos con datos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Limpia los valores X e Y de la primera serie.
series1.ClearValues();

// Rellena la serie con datos.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// Limpia los valores X e Y de la segunda serie.
series2.Clear();

// Rellena la serie con datos.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Ver también

* class [ChartSeries](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
