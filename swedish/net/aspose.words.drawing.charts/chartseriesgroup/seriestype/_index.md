---
title: ChartSeriesGroup.SeriesType
linktitle: SeriesType
articleTitle: SeriesType
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartSeriesGroup SeriesType för att enkelt identifiera diagramserietyper i dina datavisualiseringar för förbättrad analys och insikter.
type: docs
weight: 110
url: /sv/net/aspose.words.drawing.charts/chartseriesgroup/seriestype/
---
## ChartSeriesGroup.SeriesType property

Hämtar typen av diagramserie som ingår i den här gruppen.

```csharp
public ChartSeriesType SeriesType { get; }
```

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

* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeriesGroup](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
