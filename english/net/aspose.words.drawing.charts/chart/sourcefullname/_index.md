---
title: Chart.SourceFullName
linktitle: SourceFullName
second_title: Aspose.Words for .NET API Reference
description: Chart property. Gets the path and name of an xls/xlsx file this chart is linked to in C#.
type: docs
weight: 60
url: /net/aspose.words.drawing.charts/chart/sourcefullname/
---
## Chart.SourceFullName property

Gets the path and name of an xls/xlsx file this chart is linked to.

```csharp
public string SourceFullName { get; set; }
```

## Examples

Shows how to get/set the full name of the external xls/xlsx document if the chart is linked.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

var sourceFullName = shape.Chart.SourceFullName;
Assert.True(sourceFullName.Contains("Examples\\Data\\Spreadsheet.xlsx"));

sourceFullName = "D:\\Documents\\ChartData.xlsx";
Assert.True(sourceFullName.Equals("D:\\Documents\\ChartData.xlsx"));
```

### See Also

* class [Chart](../)
* namespace [Aspose.Words.Drawing.Charts](../../chart/)
* assembly [Aspose.Words](../../../)
