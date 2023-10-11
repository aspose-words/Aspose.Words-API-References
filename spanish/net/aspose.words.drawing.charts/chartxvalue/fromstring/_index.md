---
title: ChartXValue.FromString
second_title: Referencia de API de Aspose.Words para .NET
description: ChartXValue método. Crea unChartXValue instancia de laString tipo.
type: docs
weight: 40
url: /es/net/aspose.words.drawing.charts/chartxvalue/fromstring/
---
## ChartXValue.FromString method

Crea un[`ChartXValue`](../) instancia de laString tipo.

```csharp
public static ChartXValue FromString(string value)
```

### Ejemplos

Muestra cómo agregar/eliminar valores de datos del gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries department1Series = chart.Series[0];
ChartSeries department2Series = chart.Series[1];

// Elimina el primer valor de ambas series.
department1Series.Remove(0);
department2Series.Remove(0);

// Agrega nuevos valores a ambas series.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

### Ver también

* class [ChartXValue](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../chartxvalue/)
* asamblea [Aspose.Words](../../../)


