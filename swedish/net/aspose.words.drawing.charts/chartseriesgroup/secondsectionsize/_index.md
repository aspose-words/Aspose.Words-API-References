---
title: ChartSeriesGroup.SecondSectionSize
linktitle: SecondSectionSize
articleTitle: SecondSectionSize
second_title: Aspose.Words för .NET
description: Upptäck hur du justerar egenskapen SecondSectionSize i ChartSeriesGroup för att effektivt anpassa storleken på den sekundära sektionen i cirkeldiagrammet.
type: docs
weight: 90
url: /sv/net/aspose.words.drawing.charts/chartseriesgroup/secondsectionsize/
---
## ChartSeriesGroup.SecondSectionSize property

Hämtar eller ställer in storleken på cirkeldiagrammets sekundära sektion som en procentandel.

```csharp
public int SecondSectionSize { get; set; }
```

## Anmärkningar

Gäller seriegrupper avPieOfPie och PieOfBar typer.

Intervallet för acceptabla värden är från 5 till 200. Standardvärdet är 75.

## Exempel

Visar hur man skapar och formaterar ett cirkeldiagram.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.PieOfPie, 440, 300);
Chart chart = shape.Chart;
// Radera den standardgenererade serien.
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3", "Category 4" };
chart.Series.Add("Series 1", categories, new double[] { 11, 8, 4, 3 });

// Formatera cirkeldiagrammet.
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.GapWidth = 10;
seriesGroup.SecondSectionSize = 77;

doc.Save(ArtifactsDir + "Charts.PieOfPieChart.docx");
```

### Se även

* class [ChartSeriesGroup](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
