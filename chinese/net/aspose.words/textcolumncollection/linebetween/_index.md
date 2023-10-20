---
title: TextColumnCollection.LineBetween
linktitle: LineBetween
articleTitle: LineBetween
second_title: 用于 .NET 的 Aspose.Words
description: TextColumnCollection LineBetween 财产. 当真的在列之间添加一条垂直线 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words/textcolumncollection/linebetween/
---
## TextColumnCollection.LineBetween property

当`真的`，在列之间添加一条垂直线。

```csharp
public bool LineBetween { get; set; }
```

## 例子

演示如何用垂直线分隔列。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 配置当前节的PageSetup对象，将文本分为几列。
// 将“LineBetween”属性设置为“true”以在列之间放置分隔线。
// 将“LineBetween”属性设置为“false”以使列之间的空间留空。
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.LineBetween = lineBetween;
columns.SetCount(3);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 3.");

doc.Save(ArtifactsDir + "PageSetup.VerticalLineBetweenColumns.docx");
```

### 也可以看看

* class [TextColumnCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
