---
title: TextColumnCollection.LineBetween
linktitle: LineBetween
articleTitle: LineBetween
second_title: Aspose.Words for .NET
description: 使用 TextColumnCollection 的 LineBetween 属性增强布局。启用列间垂直线，打造美观有序的外观。
type: docs
weight: 40
url: /zh/net/aspose.words/textcolumncollection/linebetween/
---
## TextColumnCollection.LineBetween property

当`真的`，在列之间添加垂直线。

```csharp
public bool LineBetween { get; set; }
```

## 例子

显示如何用垂直线分隔列。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 配置当前部分的 PageSetup 对象以将文本分成几列。
// 将“LineBetween”属性设置为“true”以在列之间添加分隔线。
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
