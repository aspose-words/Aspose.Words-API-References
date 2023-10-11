---
title: TextColumn.SpaceAfter
second_title: Aspose.Words for .NET API 参考
description: TextColumn 财产. 获取或设置此列与下一列之间的间距以磅为单位最后一列不需要
type: docs
weight: 10
url: /zh/net/aspose.words/textcolumn/spaceafter/
---
## TextColumn.SpaceAfter property

获取或设置此列与下一列之间的间距（以磅为单位）。最后一列不需要。

```csharp
public double SpaceAfter { get; set; }
```

### 例子

展示如何创建间隔不均匀的列。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// 确定可用于排列列的空间量。
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// 将第一列设置为窄。
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// 设置第二列以占用页面边距内的剩余可用空间。
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### 也可以看看

* class [TextColumn](../)
* 命名空间 [Aspose.Words](../../textcolumn/)
* 部件 [Aspose.Words](../../../)


