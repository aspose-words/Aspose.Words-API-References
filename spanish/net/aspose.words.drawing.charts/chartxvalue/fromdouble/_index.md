---
title: ChartXValue.FromDouble
second_title: Referencia de API de Aspose.Words para .NET
description: ChartXValue método. Crea unChartXValue instancia de laDouble tipo.
type: docs
weight: 20
url: /es/net/aspose.words.drawing.charts/chartxvalue/fromdouble/
---
## ChartXValue.FromDouble method

Crea un[`ChartXValue`](../) instancia de laDouble tipo.

```csharp
public static ChartXValue FromDouble(double value)
```

### Ejemplos

Muestra cómo completar series de gráficos con datos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Borrar los valores X e Y de la primera serie.
series1.ClearValues();

// Completa la serie con datos.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9), ChartYValue.FromDouble(17));

ChartSeries series2 = chart.Series[1];

// Borrar los valores X e Y de la segunda serie.
series2.ClearValues();

// Completa la serie con datos.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Ver también

* class [ChartXValue](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../chartxvalue/)
* asamblea [Aspose.Words](../../../)


