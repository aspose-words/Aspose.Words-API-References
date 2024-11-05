---
title: ChartLegendEntry Class
linktitle: ChartLegendEntry
articleTitle: ChartLegendEntry
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartLegendEntry class. Represents a chart legend entry in C#.
type: docs
weight: 970
url: /net/aspose.words.drawing.charts/chartlegendentry/
---
## ChartLegendEntry class

Represents a chart legend entry.

To learn more, visit the [Working with Charts](https://docs.aspose.com/words/net/working-with-charts/) documentation article.

```csharp
public class ChartLegendEntry
```

## Properties

| Name | Description |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartlegendentry/font/) { get; } | Provides access to the font formatting of this legend entry. |
| [IsHidden](../../aspose.words.drawing.charts/chartlegendentry/ishidden/) { get; set; } | Gets or sets a value indicating whether this entry is hidden in the chart legend. The default value is **false**. |

## Remarks

A legend entry corresponds to a specific chart series or trendline.

The text of the entry is the name of the series or trendline. The text cannot be changed.

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

doc.Save(ArtifactsDir + "Charts.LegendFont.docx");
```

### See Also

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
