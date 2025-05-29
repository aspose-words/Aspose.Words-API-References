---
title: ChartDataLabelCollection.ShowCategoryName
linktitle: ShowCategoryName
articleTitle: ShowCategoryName
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ShowCategoryName i ChartDataLabelCollection. Kontrollera dataetiketternas synlighet för dina serier och förbättra diagrammets tydlighet!
type: docs
weight: 110
url: /sv/net/aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/
---
## ChartDataLabelCollection.ShowCategoryName property

Gör det möjligt att ange om kategorinamnet ska visas för dataetiketterna för hela serien. Standardvärdet är`falsk` .

```csharp
public bool ShowCategoryName { get; set; }
```

## Anmärkningar

Värde definierat för den här egenskapen kan åsidosättas för en enskild dataetikett med hjälp av [`ShowCategoryName`](../../chartdatalabel/showcategoryname/) egendom.

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
