---
title: ChartSeriesGroupCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words para .NET
description: Descubra el método ChartSeriesGroupCollection Add para agregar fácilmente nuevos grupos de series y mejorar sus capacidades de visualización de datos.
type: docs
weight: 30
url: /es/net/aspose.words.drawing.charts/chartseriesgroupcollection/add/
---
## ChartSeriesGroupCollection.Add method

Agrega un nuevo grupo de series del tipo de serie especificado a esta colección.

```csharp
public ChartSeriesGroup Add(ChartSeriesType seriesType)
```

## Observaciones

Los gráficos combinados solo pueden contener grupos de series de los siguientes tipos: área, barras, columnas, líneas, circulares, de dispersión, tipos de radar y de acciones (excepto los tipos de series 3D correspondientes).

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

* class [ChartSeriesGroup](../../chartseriesgroup/)
* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeriesGroupCollection](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
