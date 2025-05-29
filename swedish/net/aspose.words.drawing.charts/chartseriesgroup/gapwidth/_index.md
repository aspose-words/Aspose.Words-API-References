---
title: ChartSeriesGroup.GapWidth
linktitle: GapWidth
articleTitle: GapWidth
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartSeriesGroup GapWidth för att enkelt justera avståndet i procent mellan diagramelement för förbättrad datavisualisering.
type: docs
weight: 70
url: /sv/net/aspose.words.drawing.charts/chartseriesgroup/gapwidth/
---
## ChartSeriesGroup.GapWidth property

Hämtar eller ställer in procenten av mellanrumsbredden mellan diagramelement.

```csharp
public int GapWidth { get; set; }
```

## Anmärkningar

Gäller endast seriegrupper av typerna stapel, kolumn, cirkeldiagram-av-stapel, cirkeldiagram-av-paj, histogram, box&amp;whisker, vattenfall och tratt.

Intervallet för acceptabla värden är från 0 till och med 500. För stapel-/kolumnbaserade seriegrupper representerar egenskapen avståndet mellan stapelkluster som en procentandel av deras bredd. För cirkeldiagram och stapeldiagram är detta avståndet mellan diagrammets primära och sekundära sektioner.

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
