---
title: ChartLegendEntry.IsHidden
second_title: Aspose.Words för .NET API Referens
description: ChartLegendEntry fast egendom. Hämtar eller ställer in ett värde som anger om denna post är dold i diagramförklaringen. Standardvärdet är falsk .
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.charts/chartlegendentry/ishidden/
---
## ChartLegendEntry.IsHidden property

Hämtar eller ställer in ett värde som anger om denna post är dold i diagramförklaringen. Standardvärdet är **falsk** .

```csharp
public bool IsHidden { get; set; }
```

### Anmärkningar

När en diagramförklaringspost är dold påverkar den inte motsvarande diagramserie eller trendlinje som fortfarande visas på diagrammet.

### Exempel

Visar hur man arbetar med en förklaringspost för diagramserier.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "AW Category 1", "AW Category 2" };

ChartSeries series1 = series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });
series.Add("Series 3", categories, new double[] { 5, 6 });
series.Add("Series 4", categories, new double[] { 0, 0 });

ChartLegendEntryCollection legendEntries = chart.Legend.LegendEntries;
legendEntries[3].IsHidden = true;

foreach (ChartLegendEntry legendEntry in legendEntries)
    legendEntry.Font.Size = 12;

series1.LegendEntry.Font.Italic = true;

doc.Save(ArtifactsDir + "Charts.LegendEntries.docx");
```

### Se även

* class [ChartLegendEntry](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../chartlegendentry/)
* hopsättning [Aspose.Words](../../../)


