---
title: ChartLegendEntry.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words for .NET
description: Discover the ChartLegendEntry Font property for easy access to customizable font formatting, enhancing your legend entries for better visual appeal.
type: docs
weight: 10
url: /net/aspose.words.drawing.charts/chartlegendentry/font/
---
## ChartLegendEntry.Font property

Provides access to the font formatting of this legend entry.

```csharp
public Font Font { get; }
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

* class [Font](../../../aspose.words/font/)
* class [ChartLegendEntry](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
