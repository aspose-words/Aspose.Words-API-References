---
title: ChartSeries.ClearValues
linktitle: ClearValues
articleTitle: ClearValues
second_title: Aspose.Words para .NET
description: Descubra ChartSeries ClearValues. Elimine fácilmente los valores de los datos, conservando el formato y las etiquetas de su gráfico para una apariencia más limpia y profesional.
type: docs
weight: 180
url: /es/net/aspose.words.drawing.charts/chartseries/clearvalues/
---
## ChartSeries.ClearValues method

Elimina todos los valores de datos de la serie del gráfico conservando el formato de los puntos de datos y las etiquetas de datos.

```csharp
public void ClearValues()
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
