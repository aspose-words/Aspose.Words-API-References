---
title: ChartSeries.LegendEntry
linktitle: LegendEntry
articleTitle: LegendEntry
second_title: Aspose.Words for .NET
description: ChartSeries LegendEntry property. Gets a legend entry for this chart series in C#.
type: docs
weight: 90
url: /net/aspose.words.drawing.charts/chartseries/legendentry/
---
## ChartSeries.LegendEntry property

Gets a legend entry for this chart series.

```csharp
public ChartLegendEntry LegendEntry { get; }
```

## Examples

Shows how to work with a legend font.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

ChartLegend chartLegend = chart.Legend;
// Set default font size all legend entries.
chartLegend.Font.Size = 14;
// Change font for specific legend entry.
chartLegend.LegendEntries[1].Font.Italic = true;
chartLegend.LegendEntries[1].Font.Size = 12;
// Get legend entry for chart series.
ChartLegendEntry legendEntry = chart.Series[0].LegendEntry;

doc.Save(ArtifactsDir + "Charts.LegendFont.docx");
```

### See Also

* class [ChartLegendEntry](../../chartlegendentry/)
* class [ChartSeries](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
