---
title: ChartDataLabelCollection.Separator
linktitle: Separator
articleTitle: Separator
second_title: Aspose.Words för .NET
description: ChartDataLabelCollection Separator fast egendom. Hämtar eller ställer in strängseparator som används för dataetiketterna för hela serien. Standard är ett kommatecken förutom för cirkeldiagram som endast visar kategorinamn och procent då en radbrytning ska användas istället i C#.
type: docs
weight: 60
url: /sv/net/aspose.words.drawing.charts/chartdatalabelcollection/separator/
---
## ChartDataLabelCollection.Separator property

Hämtar eller ställer in strängseparator som används för dataetiketterna för hela serien. Standard är ett kommatecken, förutom för cirkeldiagram som endast visar kategorinamn och procent, då en radbrytning ska användas istället.

```csharp
public string Separator { get; set; }
```

## Anmärkningar

Värdet som definierats för den här egenskapen kan åsidosättas för en individuell dataetikett med hjälp av [`Separator`](../../chartdatalabel/separator/) egenskap.

## Exempel

Visar hur man arbetar med dataetiketter i ett bubbeldiagram.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// Rensa diagrammets demodataserie för att börja med ett rent diagram.
chart.Series.Clear();

// Lägg till en anpassad serie med X/Y-koordinater och diameter för var och en av bubblorna.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { 2.9, 3.5, 1.1, 4.0, 4.0 },
    new[] { 1.9, 8.5, 2.1, 6.0, 1.5 },
    new[] { 9.0, 4.5, 2.5, 8.0, 5.0 });

// Aktivera dataetiketter och ändra sedan deras utseende.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowBubbleSize = true;
dataLabels.ShowCategoryName = true;
dataLabels.ShowSeriesName = true;
dataLabels.Separator = " & ";

doc.Save(ArtifactsDir + "Charts.DataLabelsBubbleChart.docx");
```

Visar hur man arbetar med dataetiketter i ett cirkeldiagram.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// Rensa diagrammets demodataserie för att börja med ett rent diagram.
chart.Series.Clear();

// Infoga en anpassad diagramserie med ett kategorinamn för var och en av sektorerna och deras frekvenstabell.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// Aktivera dataetiketter som visar både procent och frekvens för varje sektor, och ändra deras utseende.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowLeaderLines = true;
dataLabels.ShowLegendKey = true;
dataLabels.ShowPercentage = true;
dataLabels.ShowValue = true;
dataLabels.Separator = "; ";

doc.Save(ArtifactsDir + "Charts.DataLabelsPieChart.docx");
```

### Se även

* class [ChartDataLabelCollection](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
