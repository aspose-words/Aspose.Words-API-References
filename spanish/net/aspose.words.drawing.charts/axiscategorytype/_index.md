---
title: Enum AxisCategoryType
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Drawing.Charts.AxisCategoryType enumeración. Especifica el tipo de un eje de categoría.
type: docs
weight: 520
url: /es/net/aspose.words.drawing.charts/axiscategorytype/
---
## AxisCategoryType enumeration

Especifica el tipo de un eje de categoría.

```csharp
public enum AxisCategoryType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Automatic | `0` | Especifica que el tipo de eje de categoría se determina automáticamente en función de los datos. |
| Category | `1` | Especifica un eje de un conjunto arbitrario de categorías. |
| Time | `2` | Especifica un eje de categoría de tiempo. |

### Ejemplos

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
// como su dirección, marcas de unidad mayor/menor y marcas de graduación.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabelOffset = 50;
xAxis.TickLabelPosition = AxisTickLabelPosition.Low;
xAxis.TickLabelSpacingIsAuto = false;
xAxis.TickMarkSpacing = 1;

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabelPosition = AxisTickLabelPosition.NextToAxis;

// Los gráficos de columnas no tienen un eje Z.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)


