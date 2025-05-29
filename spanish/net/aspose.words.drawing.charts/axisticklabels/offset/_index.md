---
title: AxisTickLabels.Offset
linktitle: Offset
articleTitle: Offset
second_title: Aspose.Words para .NET
description: Ajuste el desplazamiento de AxisTickLabels para personalizar la distancia de la etiqueta de marca desde el eje para una mayor claridad y atractivo visual en sus visualizaciones de datos.
type: docs
weight: 40
url: /es/net/aspose.words.drawing.charts/axisticklabels/offset/
---
## AxisTickLabels.Offset property

Obtiene o establece la distancia de las etiquetas de marca desde el eje.

```csharp
public int Offset { get; set; }
```

## Observaciones

La propiedad representa un porcentaje del desplazamiento de etiqueta predeterminado.

El rango válido es del 0 al 1000 % inclusive. El valor predeterminado es 100 %.

Esta propiedad solo afecta a los ejes de categorías. No es compatible con los nuevos gráficos de MS Office 2016.

## Ejemplos

Muestra cómo insertar un gráfico y modificar la apariencia de sus ejes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.Series.Clear();

// Inserte una serie de gráficos con categorías para el eje X y valores numéricos respectivos para el eje Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// Los ejes del gráfico tienen varias opciones que pueden cambiar su apariencia,
// como su dirección, marcas de unidad principales/secundarias y marcas de graduación.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabels.Offset = 50;
xAxis.TickLabels.Position = AxisTickLabelPosition.Low;
xAxis.TickLabels.IsAutoSpacing = false;
xAxis.TickMarkSpacing = 1;

Assert.AreEqual(doc, xAxis.Document);

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabels.Position = AxisTickLabelPosition.NextToAxis;
yAxis.TickLabels.Alignment = ParagraphAlignment.Center;
yAxis.TickLabels.Font.Color = Color.Red;
yAxis.TickLabels.Spacing = 1;

//Los gráficos de columnas no tienen eje Z.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Ver también

* class [AxisTickLabels](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
