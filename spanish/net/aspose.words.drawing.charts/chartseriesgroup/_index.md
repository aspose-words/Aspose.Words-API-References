---
title: ChartSeriesGroup Class
linktitle: ChartSeriesGroup
articleTitle: ChartSeriesGroup
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.Charts.ChartSeriesGroup, que simplifica la administración de las propiedades de las series de gráficos para mejorar la visualización y el análisis de datos.
type: docs
weight: 1090
url: /es/net/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class

Representa las propiedades de un grupo de series de gráficos, es decir, las propiedades de las series de gráficos del mismo tipo asociadas a los mismos ejes.

```csharp
public class ChartSeriesGroup
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AxisGroup](../../aspose.words.drawing.charts/chartseriesgroup/axisgroup/) { get; set; } | Obtiene o establece el grupo de ejes al que pertenece este grupo de series. |
| [AxisX](../../aspose.words.drawing.charts/chartseriesgroup/axisx/) { get; } | Proporciona acceso a las propiedades del eje X de este grupo de series. |
| [AxisY](../../aspose.words.drawing.charts/chartseriesgroup/axisy/) { get; } | Proporciona acceso a las propiedades del eje Y de este grupo de series. |
| [BubbleScale](../../aspose.words.drawing.charts/chartseriesgroup/bubblescale/) { get; set; } | Obtiene o establece el tamaño de las burbujas como un porcentaje de su tamaño predeterminado. |
| [DoughnutHoleSize](../../aspose.words.drawing.charts/chartseriesgroup/doughnutholesize/) { get; set; } | Obtiene o establece el tamaño del orificio del gráfico de anillos principal como un porcentaje. |
| [FirstSliceAngle](../../aspose.words.drawing.charts/chartseriesgroup/firstsliceangle/) { get; set; } | Obtiene o establece el ángulo, en grados, de la primera porción del gráfico circular principal. |
| [GapWidth](../../aspose.words.drawing.charts/chartseriesgroup/gapwidth/) { get; set; } | Obtiene o establece el porcentaje de ancho del espacio entre los elementos del gráfico. |
| [Overlap](../../aspose.words.drawing.charts/chartseriesgroup/overlap/) { get; set; } | Obtiene o establece el porcentaje de superposición de las barras o columnas de la serie. |
| [SecondSectionSize](../../aspose.words.drawing.charts/chartseriesgroup/secondsectionsize/) { get; set; } | Obtiene o establece el tamaño de la sección secundaria del gráfico circular como un porcentaje. |
| [Series](../../aspose.words.drawing.charts/chartseriesgroup/series/) { get; } | Obtiene una colección de series que pertenecen a este grupo de series. |
| [SeriesType](../../aspose.words.drawing.charts/chartseriesgroup/seriestype/) { get; } | Obtiene el tipo de serie de gráficos incluida en este grupo. |

## Observaciones

Los gráficos combinados contienen varios grupos de series de gráficos, con un grupo separado para cada tipo de serie.

También puede crear un grupo de series de gráficos para asignar ejes secundarios a una o más series de gráficos.

Para obtener más información, visite el[ Trabajando con gráficos](https://docs.aspose.com/words/net/working-with-charts/) Artículo de documentación.

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
