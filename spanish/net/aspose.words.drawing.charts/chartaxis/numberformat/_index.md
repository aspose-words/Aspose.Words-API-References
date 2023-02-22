---
title: ChartAxis.NumberFormat
second_title: Referencia de API de Aspose.Words para .NET
description: ChartAxis propiedad. Devuelve unChartNumberFormat objeto que permite definir formatos de números para el eje.
type: docs
weight: 170
url: /es/net/aspose.words.drawing.charts/chartaxis/numberformat/
---
## ChartAxis.NumberFormat property

Devuelve un[`ChartNumberFormat`](../../chartnumberformat/) objeto que permite definir formatos de números para el eje.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

### Ejemplos

Muestra cómo configurar el formato de los valores del gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.Series.Clear();

// Agregue una serie personalizada al gráfico con categorías para el eje X,
  // y grandes valores numéricos respectivos para el eje Y.
chart.Series.Add("Aspose Test Series",
    new [] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

  // Establecer el formato de número de las etiquetas de marca del eje Y para no agrupar dígitos con comas.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// Esta bandera puede anular el valor anterior y dibujar el formato de número de la celda de origen.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

### Ver también

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartAxis](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../chartaxis/)
* asamblea [Aspose.Words](../../../)


