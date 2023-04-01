---
title: Chart.Title
linktitle: Title
second_title: Aspose.Words for .NET API Reference
description: Chart property. Provides access to the chart title properties in C#.
type: docs
weight: 80
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

// Set the "Show" property to "true" to make the title visible. 
title.Show = true;

// Set the "Overlay" property to "true" Give other chart elements more room by allowing them to overlap the title
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### See Also

* class [ChartTitle](../../charttitle/)
* class [Chart](../)
* namespace [Aspose.Words.Drawing.Charts](../../chart/)
* assembly [Aspose.Words](../../../)
