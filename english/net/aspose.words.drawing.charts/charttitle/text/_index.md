---
title: ChartTitle.Text
linktitle: Text
second_title: Aspose.Words for .NET API Reference
description: ChartTitle Text property. Gets or sets the text of the chart title. If null or empty value is specified auto generated title will be shown in C#.
type: docs
weight: 30
url: /net/aspose.words.drawing.charts/charttitle/text/
---
## ChartTitle.Text property

Gets or sets the text of the chart title. If `null` or empty value is specified, auto generated title will be shown.

```csharp
public string Text { get; set; }
```

## Remarks

Use [`Show`](../show/) option if you need to hide the Title.

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

* class [ChartTitle](../)
* namespace [Aspose.Words.Drawing.Charts](../../charttitle/)
* assembly [Aspose.Words](../../../)
