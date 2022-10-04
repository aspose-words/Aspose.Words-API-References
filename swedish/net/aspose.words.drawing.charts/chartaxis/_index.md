---
title: ChartAxis
second_title: Aspose.Words för .NET API Referens
description: Representerar axelalternativen för diagrammet.
type: docs
weight: 610
url: /sv/net/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class

Representerar axelalternativen för diagrammet.

```csharp
public class ChartAxis
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AxisBetweenCategories](../../aspose.words.drawing.charts/chartaxis/axisbetweencategories/) { get; set; } | Hämtar eller sätter en flagga som indikerar om värdeaxeln korsar kategoriaxeln mellan kategorier. |
| [BaseTimeUnit](../../aspose.words.drawing.charts/chartaxis/basetimeunit/) { get; set; } | Returnerar eller ställer in den minsta tidsenheten som är representerad på tidskategoriaxeln. |
| [CategoryType](../../aspose.words.drawing.charts/chartaxis/categorytype/) { get; set; } | Hämtar eller ställer in typ av kategoriaxel. |
| [Crosses](../../aspose.words.drawing.charts/chartaxis/crosses/) { get; set; } | Anger hur denna axel korsar den vinkelräta axeln. |
| [CrossesAt](../../aspose.words.drawing.charts/chartaxis/crossesat/) { get; set; } | Anger var på den vinkelräta axeln axeln korsar. |
| [DisplayUnit](../../aspose.words.drawing.charts/chartaxis/displayunit/) { get; } | Anger skalningsvärdet för visningsenheterna för värdeaxeln. |
| [Document](../../aspose.words.drawing.charts/chartaxis/document/) { get; } | Returnerar det dokument som titelinnehavaren tillhör. |
| [Hidden](../../aspose.words.drawing.charts/chartaxis/hidden/) { get; set; } | Hämtar eller sätter en flagga som indikerar om denna axel är dold eller inte. |
| [MajorTickMark](../../aspose.words.drawing.charts/chartaxis/majortickmark/) { get; set; } | Returnerar eller sätter de viktigaste bockarna. |
| [MajorUnit](../../aspose.words.drawing.charts/chartaxis/majorunit/) { get; set; } | Returnerar eller ställer in avståndet mellan stora bockmarkeringar. |
| [MajorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/majorunitisauto/) { get; set; } | Hämtar eller ställer in en flagga som indikerar om standardavståndet mellan större bockmarkeringar ska användas. |
| [MajorUnitScale](../../aspose.words.drawing.charts/chartaxis/majorunitscale/) { get; set; } | Returnerar eller ställer in skalvärdet för stora bockmarkeringar på tidskategoriaxeln. |
| [MinorTickMark](../../aspose.words.drawing.charts/chartaxis/minortickmark/) { get; set; } | Returnerar eller ställer in de mindre bockmarkeringarna för axeln. |
| [MinorUnit](../../aspose.words.drawing.charts/chartaxis/minorunit/) { get; set; } | Returnerar eller ställer in avståndet mellan mindre bockmarkeringar. |
| [MinorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/minorunitisauto/) { get; set; } | Hämtar eller sätter en flagga som indikerar om standardavståndet mellan mindre bockmarkeringar ska användas. |
| [MinorUnitScale](../../aspose.words.drawing.charts/chartaxis/minorunitscale/) { get; set; } | Returnerar eller ställer in skalvärdet för mindre bockmarkeringar på tidskategoriaxeln. |
| [NumberFormat](../../aspose.words.drawing.charts/chartaxis/numberformat/) { get; } | Returnerar en[`ChartNumberFormat`](../chartnumberformat/) objekt som tillåter att definiera talformat för axeln. |
| [ReverseOrder](../../aspose.words.drawing.charts/chartaxis/reverseorder/) { get; set; } | Returnerar eller sätter en flagga som indikerar om värden på axeln ska visas i omvänd ordning, dvs. från max till min. |
| [Scaling](../../aspose.words.drawing.charts/chartaxis/scaling/) { get; } | Ger tillgång till skalningsalternativen för axeln. |
| [TickLabelAlignment](../../aspose.words.drawing.charts/chartaxis/ticklabelalignment/) { get; set; } | Hämtar eller ställer in textjustering av axelmarkeringsetiketter. |
| [TickLabelOffset](../../aspose.words.drawing.charts/chartaxis/ticklabeloffset/) { get; set; } | Hämtar eller ställer in etiketternas avstånd från axeln. |
| [TickLabelPosition](../../aspose.words.drawing.charts/chartaxis/ticklabelposition/) { get; set; } | Returnerar eller ställer in ticketiketternas position på axeln. |
| [TickLabelSpacing](../../aspose.words.drawing.charts/chartaxis/ticklabelspacing/) { get; set; } | Hämtar eller ställer in intervallet vid vilket bocketiketter ritas. |
| [TickLabelSpacingIsAuto](../../aspose.words.drawing.charts/chartaxis/ticklabelspacingisauto/) { get; set; } | Hämtar eller ställer in en flagga som indikerar om automatiskt intervall för att rita kryssetiketter ska användas. |
| [TickMarkSpacing](../../aspose.words.drawing.charts/chartaxis/tickmarkspacing/) { get; set; } | Hämtar eller ställer in intervallet vid vilket bockmarkeringarna dras. |
| [Type](../../aspose.words.drawing.charts/chartaxis/type/) { get; } | Returnerar typ av axel. |

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

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
