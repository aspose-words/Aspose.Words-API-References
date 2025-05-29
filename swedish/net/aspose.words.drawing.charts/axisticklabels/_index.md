---
title: AxisTickLabels Class
linktitle: AxisTickLabels
articleTitle: AxisTickLabels
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Charts.AxisTickLabels, utformad för att förbättra ditt diagrams axelmarkeringsetiketter med anpassningsbara egenskaper för bättre datavisualisering.
type: docs
weight: 840
url: /sv/net/aspose.words.drawing.charts/axisticklabels/
---
## AxisTickLabels class

Representerar egenskaper för axelmarkeringsetiketter.

```csharp
public class AxisTickLabels
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Alignment](../../aspose.words.drawing.charts/axisticklabels/alignment/) { get; set; } | Hämtar eller ställer in textjustering för axeltacketiketterna. |
| [Font](../../aspose.words.drawing.charts/axisticklabels/font/) { get; } | Ger åtkomst till teckensnittsformatering av skalstämpeletiketterna. |
| [IsAutoSpacing](../../aspose.words.drawing.charts/axisticklabels/isautospacing/) { get; set; } | Hämtar eller ställer in en flagga som anger om automatiskt intervall ska användas för att rita tick-etiketterna. |
| [Offset](../../aspose.words.drawing.charts/axisticklabels/offset/) { get; set; } | Hämtar eller ställer in avståndet mellan tick-etiketterna och axeln. |
| [Orientation](../../aspose.words.drawing.charts/axisticklabels/orientation/) { get; set; } | Hämtar eller anger orienteringen för texten i tick-etiketten. |
| [Position](../../aspose.words.drawing.charts/axisticklabels/position/) { get; set; } | Hämtar eller anger positionen för tick-etiketterna på axeln. |
| [Rotation](../../aspose.words.drawing.charts/axisticklabels/rotation/) { get; set; } | Hämtar eller ställer in rotationen av tacketiketterna i grader. |
| [Spacing](../../aspose.words.drawing.charts/axisticklabels/spacing/) { get; set; } | Hämtar eller ställer in intervallet med vilket tick-etiketterna ritas. |

## Exempel

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

// Diagramaxlar har olika alternativ som kan ändra deras utseende,
// såsom deras riktning, större/mindre enhets tick och skalmtecken.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabels.Offset = 50;
xAxis.TickLabels.Position = AxisTickLabelPosition.Low;
xAxis.TickLabels.IsAutoSpacing = false;
xAxis.TickMarkSpacing = 1;

Assert.AreEqual(doc, xAxis.Document);

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabels.Position = AxisTickLabelPosition.NextToAxis;
yAxis.TickLabels.Alignment = ParagraphAlignment.Center;
yAxis.TickLabels.Font.Color = Color.Red;
yAxis.TickLabels.Spacing = 1;

// Kolumndiagram har ingen Z-axel.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
