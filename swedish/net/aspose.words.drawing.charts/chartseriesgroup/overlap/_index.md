---
title: ChartSeriesGroup.Overlap
linktitle: Overlap
articleTitle: Overlap
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartSeriesGroup Overlap för att enkelt justera överlappningsprocenten för dina seriestaplar eller kolumner för förbättrad datavisualisering.
type: docs
weight: 80
url: /sv/net/aspose.words.drawing.charts/chartseriesgroup/overlap/
---
## ChartSeriesGroup.Overlap property

Hämtar eller ställer in procentandelen av hur mycket seriens staplar eller kolumner överlappar varandra.

```csharp
public int Overlap { get; set; }
```

## Anmärkningar

Gäller seriegrupper av alla stapel- och kolumntyper.

Intervallet för acceptabla värden är från -100 till och med 100. Värdet 0 indikerar att det inte finns något mellanrum mellan staplarna/kolumnerna. Om värdet är -100 är avståndet mellan staplarna/kolumnerna lika med deras bredd. Värdet 100 innebär att staplarna/kolumnerna överlappar varandra helt.

## Exempel

Visa hur man konfigurerar mellanrumsbredd och överlappning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// Ange kolumnmellanrumsbredd och överlappning.
seriesGroup.GapWidth = 450;
seriesGroup.Overlap = -75;

doc.Save(ArtifactsDir + "Charts.ConfigureGapOverlap.docx");
```

### Se även

* class [ChartSeriesGroup](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
