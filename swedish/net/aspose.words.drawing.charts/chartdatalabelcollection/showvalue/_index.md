---
title: ShowValue
second_title: Aspose.Words för .NET API Referens
description: Gör det möjligt att ange om värden ska visas i dataetiketterna för hela serien. Standardvärdet är falsk .
type: docs
weight: 120
url: /sv/net/aspose.words.drawing.charts/chartdatalabelcollection/showvalue/
---
## ChartDataLabelCollection.ShowValue property

Gör det möjligt att ange om värden ska visas i dataetiketterna för hela serien. Standardvärdet är **falsk** .

```csharp
public bool ShowValue { get; set; }
```

### Anmärkningar

Värdet som definierats för den här egenskapen kan åsidosättas för en individuell dataetikett med hjälp av [`ShowValue`](../../chartdatalabel/showvalue) egenskap.

### Exempel

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

* class [ChartDataLabelCollection](../../chartdatalabelcollection)
* namnutrymme [Aspose.Words.Drawing.Charts](../../chartdatalabelcollection)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->