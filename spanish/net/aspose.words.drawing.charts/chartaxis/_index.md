---
title: ChartAxis Class
linktitle: ChartAxis
articleTitle: ChartAxis
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.Charts.ChartAxis para personalizar los ejes de los gráficos. ¡Mejore la visualización de sus datos fácilmente!
type: docs
weight: 890
url: /es/net/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class

Representa las opciones del eje del gráfico.

Para obtener más información, visite el[Trabajar con gráficos](https://docs.aspose.com/words/net/working-with-charts/) Artículo de documentación.

```csharp
public class ChartAxis
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AxisBetweenCategories](../../aspose.words.drawing.charts/chartaxis/axisbetweencategories/) { get; set; } | Obtiene o establece un indicador que indica si el eje de valores cruza el eje de categorías entre categorías. |
| [BaseTimeUnit](../../aspose.words.drawing.charts/chartaxis/basetimeunit/) { get; set; } | Devuelve o establece la unidad de tiempo más pequeña que se representa en el eje de categoría de tiempo. |
| [CategoryType](../../aspose.words.drawing.charts/chartaxis/categorytype/) { get; set; } | Obtiene o establece el tipo del eje de categoría. |
| [Crosses](../../aspose.words.drawing.charts/chartaxis/crosses/) { get; set; } | Especifica cómo este eje cruza el eje perpendicular. |
| [CrossesAt](../../aspose.words.drawing.charts/chartaxis/crossesat/) { get; set; } | Especifica en qué punto del eje perpendicular se cruza el eje. |
| [DisplayUnit](../../aspose.words.drawing.charts/chartaxis/displayunit/) { get; } | Especifica el valor de escala de las unidades de visualización para el eje de valores. |
| [Document](../../aspose.words.drawing.charts/chartaxis/document/) { get; } | Devuelve el documento que contiene el gráfico principal. |
| [Format](../../aspose.words.drawing.charts/chartaxis/format/) { get; } | Proporciona acceso al formato de línea del eje y al relleno de las etiquetas de marca. |
| [HasMajorGridlines](../../aspose.words.drawing.charts/chartaxis/hasmajorgridlines/) { get; set; } | Obtiene o establece un indicador que indica si el eje tiene líneas de cuadrícula principales. |
| [HasMinorGridlines](../../aspose.words.drawing.charts/chartaxis/hasminorgridlines/) { get; set; } | Obtiene o establece un indicador que indica si el eje tiene líneas de cuadrícula menores. |
| [Hidden](../../aspose.words.drawing.charts/chartaxis/hidden/) { get; set; } | Obtiene o establece un indicador que indica si este eje está oculto o no. |
| [MajorTickMark](../../aspose.words.drawing.charts/chartaxis/majortickmark/) { get; set; } | Devuelve o establece las marcas de graduación principales. |
| [MajorUnit](../../aspose.words.drawing.charts/chartaxis/majorunit/) { get; set; } | Devuelve o establece la distancia entre las marcas de graduación principales. |
| [MajorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/majorunitisauto/) { get; set; } | Obtiene o establece un indicador que indica si se utilizará la distancia predeterminada entre las marcas de graduación principales. |
| [MajorUnitScale](../../aspose.words.drawing.charts/chartaxis/majorunitscale/) { get; set; } | Devuelve o establece el valor de escala para las marcas de graduación principales en el eje de categoría de tiempo. |
| [MinorTickMark](../../aspose.words.drawing.charts/chartaxis/minortickmark/) { get; set; } | Devuelve o establece las marcas de graduación menores para el eje. |
| [MinorUnit](../../aspose.words.drawing.charts/chartaxis/minorunit/) { get; set; } | Devuelve o establece la distancia entre marcas de graduación menores. |
| [MinorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/minorunitisauto/) { get; set; } | Obtiene o establece un indicador que indica si se debe utilizar la distancia predeterminada entre las marcas de graduación menores. |
| [MinorUnitScale](../../aspose.words.drawing.charts/chartaxis/minorunitscale/) { get; set; } | Devuelve o establece el valor de escala para las marcas de graduación menores en el eje de categoría de tiempo. |
| [NumberFormat](../../aspose.words.drawing.charts/chartaxis/numberformat/) { get; } | Devuelve un[`ChartNumberFormat`](../chartnumberformat/) objeto que permite definir formatos de números para el eje. |
| [ReverseOrder](../../aspose.words.drawing.charts/chartaxis/reverseorder/) { get; set; } | Devuelve o establece un indicador que indica si los valores del eje deben mostrarse en orden inverso, es decir, de máximo a mínimo. |
| [Scaling](../../aspose.words.drawing.charts/chartaxis/scaling/) { get; } | Proporciona acceso a las opciones de escala del eje. |
| [TickLabels](../../aspose.words.drawing.charts/chartaxis/ticklabels/) { get; } | Proporciona acceso a las propiedades de las etiquetas de las marcas de graduación del eje. |
| [TickMarkSpacing](../../aspose.words.drawing.charts/chartaxis/tickmarkspacing/) { get; set; } | Obtiene o establece el intervalo en el que se dibujan las marcas de graduación. |
| [Title](../../aspose.words.drawing.charts/chartaxis/title/) { get; } | Proporciona acceso a las propiedades del título del eje. |
| [Type](../../aspose.words.drawing.charts/chartaxis/type/) { get; } | Devuelve el tipo del eje. |

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

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
