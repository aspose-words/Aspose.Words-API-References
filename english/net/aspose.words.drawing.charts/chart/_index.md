---
title: Chart Class
linktitle: Chart
articleTitle: Chart
second_title: Aspose.Words for .NET
description: Unlock powerful chart shape properties with Aspose.Words.Drawing.Charts.Chart class. Enhance your documents with dynamic visual data representation.
type: docs
weight: 870
url: /net/aspose.words.drawing.charts/chart/
---
## Chart class

Provides access to the chart shape properties.

To learn more, visit the [Working with Charts](https://docs.aspose.com/words/net/working-with-charts/) documentation article.

```csharp
public class Chart
```

## Properties

| Name | Description |
| --- | --- |
| [Axes](../../aspose.words.drawing.charts/chart/axes/) { get; } | Gets a collection of all axes of this chart. |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | Provides access to properties of the primary X axis of the chart. |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | Provides access to properties of the primary Y axis of the chart. |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | Provides access to properties of the Z axis of the chart. |
| [DataTable](../../aspose.words.drawing.charts/chart/datatable/) { get; } | Provides access to properties of a data table of this chart. The data table can be shown using the [`Show`](../chartdatatable/show/) property. |
| [Format](../../aspose.words.drawing.charts/chart/format/) { get; } | Provides access to fill and line formatting of the chart. |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | Provides access to the chart legend properties. |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | Provides access to series collection. |
| [SeriesGroups](../../aspose.words.drawing.charts/chart/seriesgroups/) { get; } | Provides access to a series group collection of this chart. |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | Gets the path and name of an xls/xlsx file this chart is linked to. |
| [Style](../../aspose.words.drawing.charts/chart/style/) { get; set; } | Gets or sets the style of the chart. |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | Provides access to the chart title properties. |

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
