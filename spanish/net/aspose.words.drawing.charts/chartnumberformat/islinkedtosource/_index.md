---
title: ChartNumberFormat.IsLinkedToSource
linktitle: IsLinkedToSource
articleTitle: IsLinkedToSource
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad ChartNumberFormat IsLinkedToSource mejora la visualización de datos al vincular códigos de formato a las celdas de origen. ¡Obtenga más información ahora!
type: docs
weight: 20
url: /es/net/aspose.words.drawing.charts/chartnumberformat/islinkedtosource/
---
## ChartNumberFormat.IsLinkedToSource property

Especifica si el código de formato está vinculado a una celda de origen. El valor predeterminado es verdadero.

```csharp
public bool IsLinkedToSource { get; set; }
```

## Observaciones

El formato de número se restablecerá a general si el código de formato está vinculado a la fuente.

## Ejemplos

Muestra cómo establecer el formato para los valores del gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.Series.Clear();

// Agregue una serie personalizada al gráfico con categorías para el eje X,
 // y valores numéricos grandes respectivos para el eje Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // Establezca el formato de número de las etiquetas de marca del eje Y para no agrupar los dígitos con comas.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// Esta bandera puede anular el valor anterior y extraer el formato de número de la celda de origen.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

### Ver también

* class [ChartNumberFormat](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
