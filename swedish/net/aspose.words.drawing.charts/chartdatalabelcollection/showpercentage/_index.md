---
title: ChartDataLabelCollection.ShowPercentage
linktitle: ShowPercentage
articleTitle: ShowPercentage
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ShowPercentage i ChartDataLabelCollection för att förbättra dina cirkeldiagram genom att visa procentvärden för dataetiketter. Öka tydligheten och insikterna!
type: docs
weight: 150
url: /sv/net/aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/
---
## ChartDataLabelCollection.ShowPercentage property

Gör det möjligt att ange om procentvärde ska visas för dataetiketterna för hela serien. Standardvärdet är`falsk` Gäller endast cirkeldiagram.

```csharp
public bool ShowPercentage { get; set; }
```

## Anmärkningar

Värde definierat för den här egenskapen kan åsidosättas för en enskild dataetikett med hjälp av [`ShowPercentage`](../../chartdatalabel/showpercentage/) egendom.

## Exempel

Visar hur man arbetar med dataetiketter i ett cirkeldiagram.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// Rensa diagrammets demodataserie för att börja med ett rent diagram.
chart.Series.Clear();

// Infoga en anpassad diagramserie med ett kategorinamn för varje sektor och deras frekvenstabell.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// Aktivera dataetiketter som visar både procentandel och frekvens för varje sektor och ändra deras utseende.
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
