---
title: ChartTitle.Show
linktitle: Show
articleTitle: Show
second_title: Aspose.Words for .NET
description: Enhance your charts with customizable titles. Control visibility easily—default is true. Elevate your data presentation today!
type: docs
weight: 40
url: /net/aspose.words.drawing.charts/charttitle/show/
---
## ChartTitle.Show property

Determines whether the title shall be shown for this chart. Default value is `true`.

```csharp
public bool Show { get; set; }
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

* class [ChartTitle](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
