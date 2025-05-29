---
title: TextColumnCollection.EvenlySpaced
linktitle: EvenlySpaced
articleTitle: EvenlySpaced
second_title: Aspose.Words for .NET
description: 探索 TextColumnCollection 的 EvenlySpaced 属性，确保文本列宽度相等，从而实现整洁有序的布局。轻松提升您的设计！
type: docs
weight: 20
url: /zh/net/aspose.words/textcolumncollection/evenlyspaced/
---
## TextColumnCollection.EvenlySpaced property

如果文本列宽度相等且间距均匀，则为真。

```csharp
public bool EvenlySpaced { get; set; }
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

* class [TextColumnCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
