---
title: ChartSeriesGroup Class
linktitle: ChartSeriesGroup
articleTitle: ChartSeriesGroup
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Charts.ChartSeriesGroup, som förenklar hanteringen av egenskaper för diagramserier för förbättrad datavisualisering och analys.
type: docs
weight: 1090
url: /sv/net/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class

Representerar egenskaper för en diagramseriegrupp, det vill säga egenskaperna för diagramserier av samma typ associerade med samma axlar.

```csharp
public class ChartSeriesGroup
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AxisGroup](../../aspose.words.drawing.charts/chartseriesgroup/axisgroup/) { get; set; } | Hämtar eller ställer in axelgruppen som denna seriegrupp tillhör. |
| [AxisX](../../aspose.words.drawing.charts/chartseriesgroup/axisx/) { get; } | Ger åtkomst till egenskaper för X-axeln i denna seriegrupp. |
| [AxisY](../../aspose.words.drawing.charts/chartseriesgroup/axisy/) { get; } | Ger åtkomst till egenskaper för Y-axeln i denna seriegrupp. |
| [BubbleScale](../../aspose.words.drawing.charts/chartseriesgroup/bubblescale/) { get; set; } | Hämtar eller ställer in storleken på bubblorna som en procentandel av deras standardstorlek. |
| [DoughnutHoleSize](../../aspose.words.drawing.charts/chartseriesgroup/doughnutholesize/) { get; set; } | Hämtar eller ställer in hålstorleken i det överordnade ringdiagrammet som en procentandel. |
| [FirstSliceAngle](../../aspose.words.drawing.charts/chartseriesgroup/firstsliceangle/) { get; set; } | Hämtar eller ställer in vinkeln, i grader, för den första delen av det överordnade cirkeldiagrammet. |
| [GapWidth](../../aspose.words.drawing.charts/chartseriesgroup/gapwidth/) { get; set; } | Hämtar eller ställer in procenten av mellanrumsbredden mellan diagramelement. |
| [Overlap](../../aspose.words.drawing.charts/chartseriesgroup/overlap/) { get; set; } | Hämtar eller ställer in procentandelen av hur mycket seriens staplar eller kolumner överlappar varandra. |
| [SecondSectionSize](../../aspose.words.drawing.charts/chartseriesgroup/secondsectionsize/) { get; set; } | Hämtar eller ställer in storleken på cirkeldiagrammets sekundära sektion som en procentandel. |
| [Series](../../aspose.words.drawing.charts/chartseriesgroup/series/) { get; } | Hämtar en samling serier som tillhör den här seriegruppen. |
| [SeriesType](../../aspose.words.drawing.charts/chartseriesgroup/seriestype/) { get; } | Hämtar typen av diagramserie som ingår i den här gruppen. |

## Anmärkningar

Kombinationsdiagram innehåller flera diagramseriegrupper, med en separat grupp för varje serietyp.

Du kan också skapa en diagramseriegrupp för att tilldela sekundära axlar till en eller flera diagramserier.

För att lära dig mer, besök[ Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

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

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
