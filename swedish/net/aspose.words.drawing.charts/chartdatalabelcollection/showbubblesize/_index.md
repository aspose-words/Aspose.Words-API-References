---
title: ChartDataLabelCollection.ShowBubbleSize
linktitle: ShowBubbleSize
articleTitle: ShowBubbleSize
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen ShowBubbleSize i ChartDataLabelCollection förbättrar dina bubbeldiagram genom att styra dataetiketternas synlighet. Förbättra din datapresentation!
type: docs
weight: 100
url: /sv/net/aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/
---
## ChartDataLabelCollection.ShowBubbleSize property

Gör det möjligt att ange om bubbelstorleken ska visas för dataetiketterna i hela serien. Gäller endast bubbeldiagram. Standardvärdet är`falsk` .

```csharp
public bool ShowBubbleSize { get; set; }
```

## Anmärkningar

Värde definierat för den här egenskapen kan åsidosättas för en enskild dataetikett med hjälp av [`ShowBubbleSize`](../../chartdatalabel/showbubblesize/) egendom.

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

### Se även

* class [ChartDataLabelCollection](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
