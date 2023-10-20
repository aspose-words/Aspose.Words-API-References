---
title: PageSetup.TextColumns
linktitle: TextColumns
articleTitle: TextColumns
second_title: 用于 .NET 的 Aspose.Words
description: PageSetup TextColumns 财产. 返回表示文本列集的集合 在 C#.
type: docs
weight: 420
url: /zh/net/aspose.words/pagesetup/textcolumns/
---
## PageSetup.TextColumns property

返回表示文本列集的集合。

```csharp
public TextColumnCollection TextColumns { get; }
```

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

* class [TextColumnCollection](../../textcolumncollection/)
* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
