---
title: ChartStyle Enum
linktitle: ChartStyle
articleTitle: ChartStyle
second_title: Aspose.Words for .NET
description: Apply predefined chart styles in Aspose.Words. Enhance visuals with ChartStyle enum for professional document formatting.
type: docs
weight: 1120
url: /net/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enumeration

Specifies predefined styles of a chart.

```csharp
public enum ChartStyle
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Normal | `0` | Represents the default chart style. |
| Muted | `1` | A style with muted colors. |
| Saturated | `2` | A style with more saturated colors. |
| Shaded | `3` | A style with shaded data points. |
| Flat | `4` | A style with flat data points without gradient. |
| Shadowed | `5` | A style with data points having a shadow. |
| Gradient | `6` | A style with gradient fill of data points. |
| Original | `7` | A style with an original appearance of a chart. |
| Transparent1 | `8` | A style with transparent data points. |
| Transparent2 | `9` | A style with transparent data points. |
| Outline | `10` | A style with data points having no fill, but only an outline. |
| OutlineBlack | `11` | A style with black chart background, in which data points have no fill, but only an outline. |
| Black | `12` | A style with black chart background. |
| Grey | `13` | A style with gray gradient chart background. |
| Blue | `14` | A style with blue chart background. |
| ShadedPlot | `15` | A style, in which the plot area is shaded. |

## Examples

Shows how to set and get chart style.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a chart in the Black style.
builder.InsertChart(ChartType.Column, 400, 250, ChartStyle.Black);

doc.Save(ArtifactsDir + "Charts.SetChartStyle.docx");

doc = new Document(ArtifactsDir + "Charts.SetChartStyle.docx");

// Get a chart to update.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;

// Get the chart style.
Assert.That(chart.Style, Is.EqualTo(ChartStyle.Black));
```

### See Also

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
