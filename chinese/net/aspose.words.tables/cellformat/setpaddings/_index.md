---
title: CellFormat.SetPaddings
linktitle: SetPaddings
articleTitle: SetPaddings
second_title: Aspose.Words for .NET
description: 探索 CellFormat SetPaddings 方法以自定义单元格间距（以点为单位），增强布局以提高可读性和设计感。
type: docs
weight: 170
url: /zh/net/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat.SetPaddings method

设置添加到单元格内容左侧/顶部/右侧/底部的空间量（以点为单位）。

```csharp
public void SetPaddings(double leftPadding, double topPadding, double rightPadding, 
    double bottomPadding)
```

## 例子

展示如何用空格填充单元格的内容。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 设置边框和文本内容之间的填充距离（以点为单位）
 // 我们使用文档构建器创建的每个表格单元格。
builder.CellFormat.SetPaddings(5, 10, 40, 50);

// 创建一个具有一个单元格的表格，其内容将具有空白填充。
builder.StartTable();
builder.InsertCell();
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "CellFormat.Padding.docx");
```

### 也可以看看

* class [CellFormat](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
