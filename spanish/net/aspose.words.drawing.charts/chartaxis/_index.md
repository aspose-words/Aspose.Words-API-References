---
title: Class ChartAxis
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Drawing.Charts.ChartAxis clase. Representa las opciones de eje del gráfico.
type: docs
weight: 610
url: /es/net/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class

Representa las opciones de eje del gráfico.

```csharp
public class ChartAxis
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AxisBetweenCategories](../../aspose.words.drawing.charts/chartaxis/axisbetweencategories/) { get; set; } | Obtiene o establece un indicador que indica si el eje de valor cruza el eje de categoría entre categorías. |
| [BaseTimeUnit](../../aspose.words.drawing.charts/chartaxis/basetimeunit/) { get; set; } | Devuelve o establece la unidad de tiempo más pequeña que se representa en el eje de categoría de tiempo. |
| [CategoryType](../../aspose.words.drawing.charts/chartaxis/categorytype/) { get; set; } | Obtiene o establece el tipo del eje de categoría. |
| [Crosses](../../aspose.words.drawing.charts/chartaxis/crosses/) { get; set; } | Especifica cómo este eje cruza el eje perpendicular. |
| [CrossesAt](../../aspose.words.drawing.charts/chartaxis/crossesat/) { get; set; } | Especifica dónde se cruza el eje en el eje perpendicular. |
| [DisplayUnit](../../aspose.words.drawing.charts/chartaxis/displayunit/) { get; } | Especifica el valor de escala de las unidades de visualización para el eje de valores. |
| [Document](../../aspose.words.drawing.charts/chartaxis/document/) { get; } | Devuelve el Documento al que pertenece el titular. |
| [Hidden](../../aspose.words.drawing.charts/chartaxis/hidden/) { get; set; } | Obtiene o establece un indicador que indica si este eje está oculto o no. |
| [MajorTickMark](../../aspose.words.drawing.charts/chartaxis/majortickmark/) { get; set; } | Devuelve o establece las marcas principales. |
| [MajorUnit](../../aspose.words.drawing.charts/chartaxis/majorunit/) { get; set; } | Devuelve o establece la distancia entre las principales marcas. |
| [MajorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/majorunitisauto/) { get; set; } | Obtiene o establece un indicador que indica si se utilizará la distancia predeterminada entre las principales marcas. |
| [MajorUnitScale](../../aspose.words.drawing.charts/chartaxis/majorunitscale/) { get; set; } | Devuelve o establece el valor de escala para las principales marcas en el eje de categoría de tiempo. |
| [MinorTickMark](../../aspose.words.drawing.charts/chartaxis/minortickmark/) { get; set; } | Devuelve o establece las marcas menores para el eje. |
| [MinorUnit](../../aspose.words.drawing.charts/chartaxis/minorunit/) { get; set; } | Devuelve o establece la distancia entre marcas menores. |
| [MinorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/minorunitisauto/) { get; set; } | Obtiene o establece un indicador que indica si se utilizará la distancia predeterminada entre las marcas menores. |
| [MinorUnitScale](../../aspose.words.drawing.charts/chartaxis/minorunitscale/) { get; set; } | Devuelve o establece el valor de escala para las marcas menores en el eje de categoría de tiempo. |
| [NumberFormat](../../aspose.words.drawing.charts/chartaxis/numberformat/) { get; } | Devuelve un[`ChartNumberFormat`](../chartnumberformat/) objeto que permite definir formatos de números para el eje. |
| [ReverseOrder](../../aspose.words.drawing.charts/chartaxis/reverseorder/) { get; set; } | Devuelve o establece un indicador que indica si los valores del eje deben mostrarse en orden inverso, es decir, de máximo a mínimo. |
| [Scaling](../../aspose.words.drawing.charts/chartaxis/scaling/) { get; } | Da acceso a las opciones de escalado del eje. |
| [TickLabelAlignment](../../aspose.words.drawing.charts/chartaxis/ticklabelalignment/) { get; set; } | Obtiene o establece la alineación del texto de las etiquetas de marca del eje. |
| [TickLabelOffset](../../aspose.words.drawing.charts/chartaxis/ticklabeloffset/) { get; set; } | Obtiene o establece la distancia de las etiquetas desde el eje. |
| [TickLabelPosition](../../aspose.words.drawing.charts/chartaxis/ticklabelposition/) { get; set; } | Devuelve o establece la posición de las etiquetas de marca en el eje. |
| [TickLabelSpacing](../../aspose.words.drawing.charts/chartaxis/ticklabelspacing/) { get; set; } | Obtiene o establece el intervalo en el que se dibujan las etiquetas de marca. |
| [TickLabelSpacingIsAuto](../../aspose.words.drawing.charts/chartaxis/ticklabelspacingisauto/) { get; set; } | Obtiene o establece un indicador que indica si se debe usar el intervalo automático de etiquetas de marca de dibujo. |
| [TickMarkSpacing](../../aspose.words.drawing.charts/chartaxis/tickmarkspacing/) { get; set; } | Obtiene o establece el intervalo en el que se dibujan las marcas. |
| [Type](../../aspose.words.drawing.charts/chartaxis/type/) { get; } | Devuelve el tipo del eje. |

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


