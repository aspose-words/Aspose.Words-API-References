---
title: LineBetween
second_title: Aspose.Words for .NET API 参考
description: 什么时候 真的 在列之间添加一条垂直线
type: docs
weight: 40
url: /zh/net/aspose.words/textcolumncollection/linebetween/
---
## TextColumnCollection.LineBetween property

什么时候 **真的** 在列之间添加一条垂直线。

```csharp
public bool LineBetween { get; set; }
```

### 例子

显示如何用垂直线分隔列。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 配置当前section的PageSetup对象，将文本分成几列。
// 将“LineBetween”属性设置为“true”以在列之间放置分隔线。
// 将“LineBetween”属性设置为“false”以将列之间的空间留空。
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

* class [TextColumnCollection](../../textcolumncollection)
* 命名空间 [Aspose.Words](../../textcolumncollection)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
