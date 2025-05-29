---
title: AxisGroup Enum
linktitle: AxisGroup
articleTitle: AxisGroup
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.Charts.AxisGroup, su clave para administrar grupos de ejes de gráficos de manera efectiva para una mejor visualización de datos.
type: docs
weight: 800
url: /es/net/aspose.words.drawing.charts/axisgroup/
---
## AxisGroup enumeration

Representa un tipo de grupo de ejes del gráfico.

```csharp
public enum AxisGroup
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Primary | `0` | Especifica el grupo de ejes principal. |
| Secondary | `1` | Especifica el grupo de ejes secundarios. |

## Ejemplos

Muestra cómo trabajar con el eje secundario del gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 250);
Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;

//Eliminar serie generada por defecto.
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
series.Add("Series 1 of primary series group", categories, new double[] { 2, 3, 4 });
series.Add("Series 2 of primary series group", categories, new double[] { 5, 2, 3 });

//Crea un grupo de series adicional, también del tipo línea.
ChartSeriesGroup newSeriesGroup = chart.SeriesGroups.Add(ChartSeriesType.Line);
// Especifique el uso de ejes secundarios para el nuevo grupo de series.
newSeriesGroup.AxisGroup = AxisGroup.Secondary;
// Ocultar el eje X secundario.
newSeriesGroup.AxisX.Hidden = true;
// Define el título del eje Y secundario.
newSeriesGroup.AxisY.Title.Show = true;
newSeriesGroup.AxisY.Title.Text = "Secondary Y axis";

Assert.AreEqual(ChartSeriesType.Line, newSeriesGroup.SeriesType);

//Agrega una serie al nuevo grupo de series.
ChartSeries series3 =
    newSeriesGroup.Series.Add("Series of secondary series group", categories, new double[] { 13, 11, 16 });
series3.Format.Stroke.Weight = 3.5;

doc.Save(ArtifactsDir + "Charts.SecondaryAxis.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
