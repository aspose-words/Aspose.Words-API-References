---
title: ChartSeriesGroupCollection Class
linktitle: ChartSeriesGroupCollection
articleTitle: ChartSeriesGroupCollection
second_title: Aspose.Words para .NET
description: Explore la clase Aspose.Words.ChartSeriesGroupCollection, su solución ideal para administrar y organizar objetos ChartSeriesGroup sin esfuerzo.
type: docs
weight: 1100
url: /es/net/aspose.words.drawing.charts/chartseriesgroupcollection/
---
## ChartSeriesGroupCollection class

Representa una colección de[`ChartSeriesGroup`](../chartseriesgroup/) objetos.

```csharp
public class ChartSeriesGroupCollection : IEnumerable<ChartSeriesGroup>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriesgroupcollection/count/) { get; } | Devuelve el número de grupos de series en esta colección. |
| [Item](../../aspose.words.drawing.charts/chartseriesgroupcollection/item/) { get; } | Devuelve un[`ChartSeriesGroup`](../chartseriesgroup/) en el índice especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriesgroupcollection/add/)(*[ChartSeriesType](../chartseriestype/)*) | Agrega un nuevo grupo de series del tipo de serie especificado a esta colección. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriesgroupcollection/getenumerator/)() | Devuelve un objeto enumerador. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriesgroupcollection/removeat/)(*int*) | Elimina un grupo de series en el índice especificado. Se eliminarán todas las series secundarias del gráfico. |

## Observaciones

Para obtener más información, visite el[Trabajar con gráficos](https://docs.aspose.com/words/net/working-with-charts/) artículo de documentación.

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

* class [ChartSeriesGroup](../chartseriesgroup/)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
