---
title: TextColumnCollection.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: 用于 .NET 的 Aspose.Words
description: TextColumnCollection Spacing 财产. 当列均匀分布时获取或设置每列之间的间距以点为单位 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words/textcolumncollection/spacing/
---
## TextColumnCollection.Spacing property

当列均匀分布时，获取或设置每列之间的间距（以点为单位）。

```csharp
public double Spacing { get; set; }
```

## 评论

仅在以下情况下有效[`EvenlySpaced`](../evenlyspaced/)被设定为`真的`.

## 例子

演示如何在一个部分中创建多个均匀间隔的列。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### 也可以看看

* class [TextColumnCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
