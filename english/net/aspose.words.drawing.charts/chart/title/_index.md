---
title: Chart.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words for .NET
description: Discover the Chart Title property for easy customization and enhanced visuals. Unlock your charts' full potential with user-friendly features!
type: docs
weight: 120
url: /net/aspose.words.drawing.charts/chart/title/
---
## Chart.Title property

Provides access to the chart title properties.

```csharp
public ChartTitle Title { get; }
```

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

* class [ChartTitle](../../charttitle/)
* class [Chart](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
