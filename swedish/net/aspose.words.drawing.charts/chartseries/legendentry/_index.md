---
title: ChartSeries.LegendEntry
linktitle: LegendEntry
articleTitle: LegendEntry
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartSeries LegendEntry för att enkelt komma åt och anpassa förklaringsposter för dina diagram, vilket förbättrar din datavisualisering.
type: docs
weight: 90
url: /sv/net/aspose.words.drawing.charts/chartseries/legendentry/
---
## ChartSeries.LegendEntry property

Hämtar en förklaringspost för den här diagramserien.

```csharp
public ChartLegendEntry LegendEntry { get; }
```

## Exempel

Visar hur man arbetar med ett teckensnitt för förklaringar.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

ChartLegend chartLegend = chart.Legend;
// Ange standardteckenstorlek för alla förklaringar.
chartLegend.Font.Size = 14;
// Ändra teckensnitt för specifik förklaring.
chartLegend.LegendEntries[1].Font.Italic = true;
chartLegend.LegendEntries[1].Font.Size = 12;
// Hämta förklaringspost för diagramserier.
ChartLegendEntry legendEntry = chart.Series[0].LegendEntry;

doc.Save(ArtifactsDir + "Charts.LegendFont.docx");
```

### Se även

* class [ChartLegendEntry](../../chartlegendentry/)
* class [ChartSeries](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
