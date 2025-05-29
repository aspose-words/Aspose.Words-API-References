---
title: TextColumn.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: Aspose.Words for .NET
description: 探索 TextColumn SpaceAfter 属性，轻松调整布局中列之间的间距。提升可读性，精准设计！
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

展示如何创建间距不均匀的列。

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

// 将第一列设置为窄列。
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// 设置第二列以占据页面边缘内剩余的可用空间。
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
