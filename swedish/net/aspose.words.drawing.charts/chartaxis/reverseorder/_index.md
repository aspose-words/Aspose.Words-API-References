---
title: ChartAxis.ReverseOrder
second_title: Aspose.Words för .NET API Referens
description: ChartAxis fast egendom. Returnerar eller sätter en flagga som indikerar om värden på axeln ska visas i omvänd ordning dvs. från max till min.
type: docs
weight: 180
url: /sv/net/aspose.words.drawing.charts/chartaxis/reverseorder/
---
## ChartAxis.ReverseOrder property

Returnerar eller sätter en flagga som indikerar om värden på axeln ska visas i omvänd ordning, dvs. från max till min.

```csharp
public bool ReverseOrder { get; set; }
```

### Anmärkningar

Egenskapen stöds inte av MS Office 2016 nya diagram. Standardvärdet är **falsk** .

### Exempel

Visar hur man infogar ett diagram och ändrar utseendet på dess axlar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Rensa diagrammets demodataserie för att börja med ett rent diagram.
chart.Series.Clear();

// Infoga en diagramserie med kategorier för X-axeln och respektive numeriska värden för Y-axeln.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// Diagramaxlar har olika alternativ som kan ändra utseende,
// som t.ex. deras riktning, större/mindre enhetsmarkeringar och bockmarkeringar.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabelOffset = 50;
xAxis.TickLabelPosition = AxisTickLabelPosition.Low;
xAxis.TickLabelSpacingIsAuto = false;
xAxis.TickMarkSpacing = 1;

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabelPosition = AxisTickLabelPosition.NextToAxis;

// Kolumndiagram har ingen Z-axel.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Se även

* class [ChartAxis](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../chartaxis/)
* hopsättning [Aspose.Words](../../../)


