---
title: Chart.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words for .NET
description: 发现 Chart SourceFullName 属性，轻松访问链接的 XLS/XLSX 文件的路径和名称，以增强数据可视化。
type: docs
weight: 100
url: /zh/net/aspose.words.drawing.charts/chart/sourcefullname/
---
## Chart.SourceFullName property

获取此图表链接到的 xls/xlsx 文件的路径和名称。

```csharp
public string SourceFullName { get; set; }
```

## 例子

显示如何在图表链接的情况下获取/设置外部 xls/xlsx 文档的全名。

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

var sourceFullName = shape.Chart.SourceFullName;
Assert.True(sourceFullName.Contains("Examples\\Data\\Spreadsheet.xlsx"));
```

### 也可以看看

* class [Chart](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
