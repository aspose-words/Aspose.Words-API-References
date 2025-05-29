---
title: Chart.SeriesGroups
linktitle: SeriesGroups
articleTitle: SeriesGroups
second_title: Aspose.Words för .NET
description: Utforska egenskapen Diagramseriegrupper för enkel åtkomst till en omfattande samling seriegrupper, vilket förbättrar din datavisualiseringsupplevelse.
type: docs
weight: 90
url: /sv/net/aspose.words.drawing.charts/chart/seriesgroups/
---
## Chart.SeriesGroups property

Ger åtkomst till en seriegruppsamling av detta diagram.

```csharp
public ChartSeriesGroupCollection SeriesGroups { get; }
```

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

* class [ChartSeriesGroupCollection](../../chartseriesgroupcollection/)
* class [Chart](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
