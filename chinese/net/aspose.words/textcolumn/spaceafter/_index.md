---
title: TextColumn.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: 用于 .NET 的 Aspose.Words
description: TextColumn SpaceAfter 财产. 获取或设置此列与下一列之间的间距以磅为单位最后一列不需要 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words/textcolumn/spaceafter/
---
## TextColumn.SpaceAfter property

获取或设置此列与下一列之间的间距（以磅为单位）。最后一列不需要。

```csharp
public double SpaceAfter { get; set; }
```

## 例子

显示如何创建不均匀间隔的列。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// 确定我们可用于排列列的空间量。
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// 将第一列设置为窄。
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// 将第二列设置为占用页面边缘内剩余的可用空间。
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### 也可以看看

* class [TextColumn](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
