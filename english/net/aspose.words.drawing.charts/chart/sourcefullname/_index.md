---
title: Chart.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words for .NET
description: Chart SourceFullName property. Gets the path and name of an xls/xlsx file this chart is linked to in C#.
type: docs
weight: 100
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
```

### See Also

* class [Chart](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
