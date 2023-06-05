---
title: ChartXValue.FromString
linktitle: FromString
articleTitle: FromString
second_title: Aspose.Words for .NET
description: ChartXValue FromString method. Creates a ChartXValue instance of the String type in C#.
type: docs
weight: 40
url: /net/aspose.words.drawing.charts/chartxvalue/fromstring/
---
## ChartXValue.FromString method

Creates a [`ChartXValue`](../) instance of the String type.

```csharp
public static ChartXValue FromString(string value)
```

## Examples

Shows how to add/remove chart data values.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries department1Series = chart.Series[0];
ChartSeries department2Series = chart.Series[1];

// Remove the first value in the both series.
department1Series.Remove(0);
department2Series.Remove(0);

// Add new values to the both series.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

### See Also

* class [ChartXValue](../)
* namespace [Aspose.Words.Drawing.Charts](../../chartxvalue/)
* assembly [Aspose.Words](../../../)
