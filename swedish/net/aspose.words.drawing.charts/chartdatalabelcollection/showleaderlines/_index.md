---
title: ChartDataLabelCollection.ShowLeaderLines
linktitle: ShowLeaderLines
articleTitle: ShowLeaderLines
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ShowLeaderLines i ChartDataLabelCollection för att förbättra dina datavisualiseringar. Kontrollera enkelt riktlinjer för tydligare insikter!
type: docs
weight: 130
url: /sv/net/aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/
---
## ChartDataLabelCollection.ShowLeaderLines property

Gör det möjligt att ange om hänvisningslinjer för dataetiketter ska visas för dataetiketterna i hela serien. Standardvärdet är`falsk` .

```csharp
public bool ShowLeaderLines { get; set; }
```

## Anmärkningar

Gäller endast cirkeldiagram. Hänvisningslinjer skapar en visuell koppling mellan en dataetikett och motsvarande datapunkt.

Värde som definierats för den här egenskapen kan åsidosättas för en enskild dataetikett med hjälp av the [`ShowLeaderLines`](../../chartdatalabel/showleaderlines/) egendom.

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
