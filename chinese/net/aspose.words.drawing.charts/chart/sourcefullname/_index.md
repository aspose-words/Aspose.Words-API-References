---
title: Chart.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: 用于 .NET 的 Aspose.Words
description: Chart SourceFullName 财产. 获取此图表链接到的 xls/xlsx 文件的路径和名称 在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words.drawing.charts/chart/sourcefullname/
---
## Chart.SourceFullName property

获取此图表链接到的 xls/xlsx 文件的路径和名称。

```csharp
public string SourceFullName { get; set; }
```

## 例子

显示如果图表已链接，如何获取外部 xls/xlsx 文档的全名。

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.True(shape.Chart.SourceFullName.Contains("Examples\\Data\\Spreadsheet.xlsx"));
```

### 也可以看看

* class [Chart](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
