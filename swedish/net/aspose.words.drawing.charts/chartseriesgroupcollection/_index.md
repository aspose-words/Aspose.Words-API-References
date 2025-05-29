---
title: ChartSeriesGroupCollection Class
linktitle: ChartSeriesGroupCollection
articleTitle: ChartSeriesGroupCollection
second_title: Aspose.Words för .NET
description: Utforska klassen Aspose.Words.ChartSeriesGroupCollection, din lösning för att enkelt hantera och organisera ChartSeriesGroup-objekt.
type: docs
weight: 1100
url: /sv/net/aspose.words.drawing.charts/chartseriesgroupcollection/
---
## ChartSeriesGroupCollection class

Representerar en samling av[`ChartSeriesGroup`](../chartseriesgroup/) objekt.

```csharp
public class ChartSeriesGroupCollection : IEnumerable<ChartSeriesGroup>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriesgroupcollection/count/) { get; } | Returnerar antalet seriegrupper i denna samling. |
| [Item](../../aspose.words.drawing.charts/chartseriesgroupcollection/item/) { get; } | Returnerar en[`ChartSeriesGroup`](../chartseriesgroup/) vid det angivna indexet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriesgroupcollection/add/)(*[ChartSeriesType](../chartseriestype/)*) | Lägger till en ny seriegrupp av den angivna serietypen till den här samlingen. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriesgroupcollection/getenumerator/)() | Returnerar ett uppräknarobjekt. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriesgroupcollection/removeat/)(*int*) | Tar bort en seriegrupp vid det angivna indexet. Alla underserier tas bort från diagrammet. |

## Anmärkningar

För att läsa mer, besök[Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

## Exempel

Visar hur man arbetar med diagrammets sekundära axel.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 250);
Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;

// Radera standardgenererad serie.
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
series.Add("Series 1 of primary series group", categories, new double[] { 2, 3, 4 });
series.Add("Series 2 of primary series group", categories, new double[] { 5, 2, 3 });

// Skapa en ytterligare seriegrupp, också av linjetypen.
ChartSeriesGroup newSeriesGroup = chart.SeriesGroups.Add(ChartSeriesType.Line);
// Ange användningen av sekundäraxlar för den nya seriegruppen.
newSeriesGroup.AxisGroup = AxisGroup.Secondary;
// Dölj den sekundära X-axeln.
newSeriesGroup.AxisX.Hidden = true;
// Definiera titeln för den sekundära Y-axeln.
newSeriesGroup.AxisY.Title.Show = true;
newSeriesGroup.AxisY.Title.Text = "Secondary Y axis";

Assert.AreEqual(ChartSeriesType.Line, newSeriesGroup.SeriesType);

// Lägg till en serie i den nya seriegruppen.
ChartSeries series3 =
    newSeriesGroup.Series.Add("Series of secondary series group", categories, new double[] { 13, 11, 16 });
series3.Format.Stroke.Weight = 3.5;

doc.Save(ArtifactsDir + "Charts.SecondaryAxis.docx");
```

### Se även

* class [ChartSeriesGroup](../chartseriesgroup/)
* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
