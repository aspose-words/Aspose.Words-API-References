---
title: ChartXValue.FromString
linktitle: FromString
articleTitle: FromString
second_title: Aspose.Words para .NET
description: Descubra el método ChartXValue FromString para crear fácilmente instancias de ChartXValue de tipo String. ¡Mejore su visualización de datos hoy mismo!
type: docs
weight: 40
url: /es/net/aspose.words.drawing.charts/chartxvalue/fromstring/
---
## ChartXValue.FromString method

Crea un[`ChartXValue`](../) instancia de laString tipo.

```csharp
public static ChartXValue FromString(string value)
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

* class [ChartXValue](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
