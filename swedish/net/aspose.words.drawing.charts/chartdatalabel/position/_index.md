---
title: ChartDataLabel.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartDataLabel Position för att enkelt anpassa din dataetiketts position för förbättrad datavisualisering och tydlighet.
type: docs
weight: 100
url: /sv/net/aspose.words.drawing.charts/chartdatalabel/position/
---
## ChartDataLabel.Position property

Hämtar eller anger positionen för dataetiketten.

```csharp
public ChartDataLabelPosition Position { get; set; }
```

## Anmärkningar

Positionen kan anges för dataetiketter av följande diagramserietyper:

-Bar ,Column , Histogram ,Pareto , Waterfall tillåtna värden:Center , InsideBase ,InsideEnd och OutsideEnd;

-BarStacked ,BarPercentStacked , ColumnStacked ,ColumnPercentStacked ; allowed värden:Center ,InsideBase ochInsideEnd;

-Bubble ,Bubble3D , Line ,LineStacked , LinePercentStacked ,Scatter , Stock tillåtna värden:Center , Left ,Right , Above ochBelow;

-Pie ,Pie3D , PieOfBar ,PieOfPie tillåtna värden: Center ,InsideEnd , OutsideEnd ochBestFit;

-BoxAndWhisker tillåtna värden: Left ,Right , Above ochBelow.

## Exempel

Visar hur man ställer in positionen för dataetiketten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga kolumndiagram.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Radera standardgenererad serie.
seriesColl.Clear();

// Lägg till serie.
ChartSeries series = seriesColl.Add(
    "Series 1",
    new string[] { "Category 1", "Category 2", "Category 3" },
    new double[] { 4, 5, 6 });

// Visa dataetiketter och ange teckenfärg.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.Font.Color = Color.White;

// Ange dataetikettens position.
dataLabels.Position = ChartDataLabelPosition.InsideBase;
dataLabels[0].Position = ChartDataLabelPosition.OutsideEnd;
dataLabels[0].Font.Color = Color.DarkRed;

doc.Save(ArtifactsDir + "Charts.LabelPosition.docx");
```

### Se även

* enum [ChartDataLabelPosition](../../chartdatalabelposition/)
* class [ChartDataLabel](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
