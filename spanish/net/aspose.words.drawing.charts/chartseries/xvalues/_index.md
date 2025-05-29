---
title: ChartSeries.XValues
linktitle: XValues
articleTitle: XValues
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartSeries XValues para acceder a una poderosa colección de valores X, mejorando la visualización y el análisis de sus datos.
type: docs
weight: 140
url: /es/net/aspose.words.drawing.charts/chartseries/xvalues/
---
## ChartSeries.XValues property

Obtiene una colección de valores X para esta serie de gráficos.

```csharp
public ChartXValueCollection XValues { get; }
```

## Ejemplos

Muestra cómo trabajar con el código de formato de los datos del gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar un gráfico de burbujas.
Shape shape = builder.InsertChart(ChartType.Bubble, 432, 252);
Chart chart = shape.Chart;

//Eliminar serie generada por defecto.
chart.Series.Clear();

ChartSeries series = chart.Series.Add(
    "Series1",
    new double[] { 1, 1.9, 2.45, 3 },
    new double[] { 1, -0.9, 1.82, 0 },
    new double[] { 2, 1.1, 2.95, 2 });

// Mostrar etiquetas de datos.
series.HasDataLabels = true;
series.DataLabels.ShowCategoryName = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowBubbleSize = true;

// Establecer códigos de formato de datos.
series.XValues.FormatCode = "#,##0.0#";
series.YValues.FormatCode = "#,##0.0#;[Red]\\-#,##0.0#";
series.BubbleSizes.FormatCode = "#,##0.0#";

doc.Save(ArtifactsDir + "Charts.FormatCode.docx");
```

### Ver también

* class [ChartXValueCollection](../../chartxvaluecollection/)
* class [ChartSeries](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
