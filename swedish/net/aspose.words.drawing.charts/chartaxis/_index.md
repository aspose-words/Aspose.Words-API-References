---
title: ChartAxis Class
linktitle: ChartAxis
articleTitle: ChartAxis
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Charts.ChartAxis för anpassningsbara diagramaxelalternativ. Förbättra din datavisualisering utan ansträngning!
type: docs
weight: 890
url: /sv/net/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class

Representerar axelalternativen i diagrammet.

För att lära dig mer, besök[Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public class ChartAxis
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AxisBetweenCategories](../../aspose.words.drawing.charts/chartaxis/axisbetweencategories/) { get; set; } | Hämtar eller ställer in en flagga som anger om värdeaxeln korsar kategoriaxeln mellan kategorier. |
| [BaseTimeUnit](../../aspose.words.drawing.charts/chartaxis/basetimeunit/) { get; set; } | Returnerar eller anger den minsta tidsenheten som representeras på tidskategoriaxeln. |
| [CategoryType](../../aspose.words.drawing.charts/chartaxis/categorytype/) { get; set; } | Hämtar eller anger typ för kategoriaxeln. |
| [Crosses](../../aspose.words.drawing.charts/chartaxis/crosses/) { get; set; } | Anger hur denna axel korsar den vinkelräta axeln. |
| [CrossesAt](../../aspose.words.drawing.charts/chartaxis/crossesat/) { get; set; } | Anger var axeln skärs på den vinkelräta axeln. |
| [DisplayUnit](../../aspose.words.drawing.charts/chartaxis/displayunit/) { get; } | Anger skalningsvärdet för visningsenheterna för värdeaxeln. |
| [Document](../../aspose.words.drawing.charts/chartaxis/document/) { get; } | Returnerar dokumentet som innehåller det överordnade diagrammet. |
| [Format](../../aspose.words.drawing.charts/chartaxis/format/) { get; } | Ger åtkomst till linjeformatering av axeln och fyllning av skalstrecketiketterna. |
| [HasMajorGridlines](../../aspose.words.drawing.charts/chartaxis/hasmajorgridlines/) { get; set; } | Hämtar eller ställer in en flagga som anger om axeln har större rutnät. |
| [HasMinorGridlines](../../aspose.words.drawing.charts/chartaxis/hasminorgridlines/) { get; set; } | Hämtar eller ställer in en flagga som anger om axeln har mindre stödlinjer. |
| [Hidden](../../aspose.words.drawing.charts/chartaxis/hidden/) { get; set; } | Hämtar eller ställer in en flagga som anger om denna axel är dold eller inte. |
| [MajorTickMark](../../aspose.words.drawing.charts/chartaxis/majortickmark/) { get; set; } | Returnerar eller anger de viktigaste skalmarkeringarna. |
| [MajorUnit](../../aspose.words.drawing.charts/chartaxis/majorunit/) { get; set; } | Returnerar eller anger avståndet mellan större skalstreck. |
| [MajorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/majorunitisauto/) { get; set; } | Hämtar eller ställer in en flagga som anger om standardavståndet mellan större skalstreck ska användas. |
| [MajorUnitScale](../../aspose.words.drawing.charts/chartaxis/majorunitscale/) { get; set; } | Returnerar eller ställer in skalvärdet för större skalmärken på tidskategoriaxeln. |
| [MinorTickMark](../../aspose.words.drawing.charts/chartaxis/minortickmark/) { get; set; } | Returnerar eller anger de mindre skalmarkeringarna för axeln. |
| [MinorUnit](../../aspose.words.drawing.charts/chartaxis/minorunit/) { get; set; } | Returnerar eller anger avståndet mellan mindre skalmarkeringar. |
| [MinorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/minorunitisauto/) { get; set; } | Hämtar eller ställer in en flagga som anger om standardavståndet mellan mindre skalmarkeringar ska användas. |
| [MinorUnitScale](../../aspose.words.drawing.charts/chartaxis/minorunitscale/) { get; set; } | Returnerar eller ställer in skalningsvärdet för mindre skalmärken på tidskategoriaxeln. |
| [NumberFormat](../../aspose.words.drawing.charts/chartaxis/numberformat/) { get; } | Returnerar en[`ChartNumberFormat`](../chartnumberformat/) objekt som tillåter definition av talformat för axeln. |
| [ReverseOrder](../../aspose.words.drawing.charts/chartaxis/reverseorder/) { get; set; } | Returnerar eller sätter en flagga som anger om axelvärden ska visas i omvänd ordning, t.ex. från max till min. |
| [Scaling](../../aspose.words.drawing.charts/chartaxis/scaling/) { get; } | Ger åtkomst till axelns skalningsalternativ. |
| [TickLabels](../../aspose.words.drawing.charts/chartaxis/ticklabels/) { get; } | Ger åtkomst till egenskaperna för axelns tickmarkeringsetiketter. |
| [TickMarkSpacing](../../aspose.words.drawing.charts/chartaxis/tickmarkspacing/) { get; set; } | Hämtar eller ställer in intervallet vid vilket skalstreck ritas. |
| [Title](../../aspose.words.drawing.charts/chartaxis/title/) { get; } | Ger åtkomst till axeltitelegenskaperna. |
| [Type](../../aspose.words.drawing.charts/chartaxis/type/) { get; } | Returnerar axelns typ. |

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
