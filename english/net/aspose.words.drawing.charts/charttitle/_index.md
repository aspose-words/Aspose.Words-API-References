---
title: ChartTitle Class
linktitle: ChartTitle
articleTitle: ChartTitle
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Drawing.Charts.ChartTitle class to easily manage and customize your chart titles for enhanced data visualization.
type: docs
weight: 1140
url: /net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

Provides access to the chart title properties.

To learn more, visit the [Working with Charts](https://docs.aspose.com/words/net/working-with-charts/) documentation article.

```csharp
public class ChartTitle
```

## Properties

| Name | Description |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/charttitle/font/) { get; } | Provides access to the font formatting of the chart title. |
| [Format](../../aspose.words.drawing.charts/charttitle/format/) { get; } | Provides access to fill and line formatting of the chart title. |
| [Orientation](../../aspose.words.drawing.charts/charttitle/orientation/) { get; set; } | Gets or sets the orientation of the chart title text. |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | Determines whether other chart elements shall be allowed to overlap title. By default overlay is `false`. |
| [Rotation](../../aspose.words.drawing.charts/charttitle/rotation/) { get; set; } | Gets or sets the rotation of the chart title in degrees. |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | Determines whether the title shall be shown for this chart. Default value is `true`. |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | Gets or sets the text of the chart title. If `null` or empty value is specified, auto generated title will be shown. |

## Examples

Shows how to insert a chart and set a title.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a chart shape with a document builder and get its chart.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Use the "Title" property to give our chart a title, which appears at the top center of the chart area.
ChartTitle title = chart.Title;
title.Text = "My Chart";
title.Font.Size = 15;
title.Font.Color = Color.Blue;

// Set the "Show" property to "true" to make the title visible. 
title.Show = true;

// Set the "Overlay" property to "true" Give other chart elements more room by allowing them to overlap the title
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### See Also

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
