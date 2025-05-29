---
title: ChartSeries.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words para .NET
description: Elimine fácilmente los valores X, Y y el tamaño de las burbujas de sus series de gráficos con el método ChartSeries Remove. ¡Optimice su visualización de datos hoy mismo!
type: docs
weight: 210
url: /es/net/aspose.words.drawing.charts/chartseries/remove/
---
## ChartSeries.Remove method

Elimina el valor X, el valor Y y el tamaño de burbuja, si es compatible, de la serie del gráfico en el índice especificado. También se eliminan el punto de datos y la etiqueta de datos correspondientes.

```csharp
public void Remove(int index)
```

## Ejemplos

Muestra cómo agregar o eliminar valores de datos del gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries department1Series = chart.Series[0];
ChartSeries department2Series = chart.Series[1];

//Elimina el primer valor de ambas series.
department1Series.Remove(0);
department2Series.Remove(0);

//Agrega nuevos valores a ambas series.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

### Ver también

* class [ChartSeries](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
